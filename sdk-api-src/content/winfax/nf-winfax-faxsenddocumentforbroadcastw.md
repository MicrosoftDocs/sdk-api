---
UID: NF:winfax.FaxSendDocumentForBroadcastW
title: FaxSendDocumentForBroadcastW function
author: windows-sdk-content
description: A fax client application calls the FaxSendDocumentForBroadcast function to queue several fax jobs that will transmit the same outgoing fax transmission to several recipients.
old-location: fax\_mfax_faxsenddocumentforbroadcast.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0sz8.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FaxSendDocumentForBroadcast, FaxSendDocumentForBroadcast function [Fax Service], FaxSendDocumentForBroadcastA, FaxSendDocumentForBroadcastW, _mfax_faxsenddocumentforbroadcast, fax._mfax_faxsenddocumentforbroadcast, winfax/FaxSendDocumentForBroadcast, winfax/FaxSendDocumentForBroadcastA, winfax/FaxSendDocumentForBroadcastW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSendDocumentForBroadcastW (Unicode) and FaxSendDocumentForBroadcastA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxSendDocumentForBroadcast
 - FaxSendDocumentForBroadcastA
 - FaxSendDocumentForBroadcastW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FaxSendDocumentForBroadcastW
: 
---

# FaxSendDocumentForBroadcastW function


## -description


A fax client application calls the <b>FaxSendDocumentForBroadcast</b> function to queue several fax jobs that will transmit the same outgoing fax transmission to several recipients.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param FileName [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the fully qualified path and name of the file that contains the fax document to transmit to all recipients. The path can be a UNC path or a path that begins with a drive letter. 

                    



This parameter can contain any valid local file name. The file must be a properly registered file type, and the fax server must be able to access the file.
                


### -param FaxJobId [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the unique number that identifies the queued job that will send the fax transmission.


### -param FaxRecipientCallback [in]

Type: <b>PFAX_RECIPIENT_CALLBACK</b>

Pointer to a <a href="https://msdn.microsoft.com/a20e04a0-99ed-44e5-9bff-c0d42ef0f8be">FAX_RECIPIENT_CALLBACK</a> function that retrieves user-specific information for each designated recipient of the fax transmission. The <b>FaxSendDocumentForBroadcast</b> function calls the <b>FAX_RECIPIENT_CALLBACK</b> function once for each fax recipient until it returns a value of zero, indicating that all outbound transmissions have been queued.


### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. <b>FaxSendDocumentForBroadcast</b> passes this data to the <a href="https://msdn.microsoft.com/a20e04a0-99ed-44e5-9bff-c0d42ef0f8be">FAX_RECIPIENT_CALLBACK</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>FaxHandle</i>, <i>FileName</i>, <i>FaxRecipientCallback</i>, or <i>FaxJobId</i> parameters are <b>NULL</b>, or the <b>RecipientNumber</b> member in the <a href="https://msdn.microsoft.com/d589a255-abe2-49d5-b593-3a60cdaf61eb">FAX_JOB_PARAM</a> structure is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot locate the file specified by the <i>FileName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot render the file specified by the <i>FileName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_JOB_SUBMIT</a> access is required.

</td>
</tr>
</table>
 




## -remarks



The function calls the <a href="https://msdn.microsoft.com/a20e04a0-99ed-44e5-9bff-c0d42ef0f8be">FAX_RECIPIENT_CALLBACK</a> function once for each designated fax recipient.

An application should call the <b>FaxSendDocumentForBroadcast</b> function to efficiently send a fax document to multiple recipients, rather than calling <a href="https://msdn.microsoft.com/bbf8def4-4af0-4315-94f9-860f9db1eefa">FaxSendDocument</a> multiple times. This is because <b>FaxSendDocumentForBroadcast</b> stores the master document only once, using the same file for all outbound transmissions.

<div class="alert"><b>Note</b>  To send a fax document efficiently to multiple recipients, an application should call the <a href="https://msdn.microsoft.com/bbf8def4-4af0-4315-94f9-860f9db1eefa">FaxSendDocument</a> function multiple times. The <b>FaxSendDocumentForBroadcast</b> function is supported for backward compatibility.</div>
<div> </div>
The <b>FaxSendDocumentForBroadcast</b> function performs the following operations in the order indicated:

<ol>
<li>The function queues the master document for transmission to multiple fax transmission recipients.</li>
<li>The function calls the user-defined <a href="https://msdn.microsoft.com/a20e04a0-99ed-44e5-9bff-c0d42ef0f8be">FAX_RECIPIENT_CALLBACK</a> function. If the callback function supplies the required information for the transmission to a fax recipient, it returns a value of nonzero. This value indicates that <b>FaxSendDocumentForBroadcast</b> should use the data to queue an outbound fax.</li>
<li>The function queues a fax transmission job for the first recipient using the master document.</li>
<li>The function calls the <a href="https://msdn.microsoft.com/a20e04a0-99ed-44e5-9bff-c0d42ef0f8be">FAX_RECIPIENT_CALLBACK</a> function multiple times, until it returns a value of zero. Each time <b>FAX_RECIPIENT_CALLBACK</b> returns nonzero, the <b>FaxSendDocumentForBroadcast</b> function queues an outbound transmission for the next fax recipient. A value of zero indicates that there are no more fax transmission jobs to queue, and calls to <b>FAX_RECIPIENT_CALLBACK</b> should be terminated.</li>
</ol>
For more information, see <a href="https://msdn.microsoft.com/bee4d50b-d6e3-432b-9db6-c7df837079f4">Transmitting Faxes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a20e04a0-99ed-44e5-9bff-c0d42ef0f8be">FAX_RECIPIENT_CALLBACK</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/bbf8def4-4af0-4315-94f9-860f9db1eefa">FaxSendDocument</a>
 

 

