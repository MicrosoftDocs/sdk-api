---
UID: NF:winfax.FaxSendDocumentA
title: FaxSendDocumentA function
author: windows-sdk-content
description: A fax client application calls the FaxSendDocument function to queue a fax job that will transmit an outgoing fax transmission.
old-location: fax\_mfax_faxsenddocument.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7t6c.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FaxSendDocument, FaxSendDocument function [Fax Service], FaxSendDocumentA, FaxSendDocumentW, _mfax_faxsenddocument, fax._mfax_faxsenddocument, winfax/FaxSendDocument, winfax/FaxSendDocumentA, winfax/FaxSendDocumentW
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
req.unicode-ansi: FaxSendDocumentW (Unicode) and FaxSendDocumentA (ANSI)
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
 - FaxSendDocument
 - FaxSendDocumentA
 - FaxSendDocumentW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxSendDocumentA function


## -description


A fax client application calls the <b>FaxSendDocument</b> function to queue a fax job that will transmit an outgoing fax transmission.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param FileName [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the fully qualified path and name of the file that contains the fax document to transmit. The path can be a UNC path or a path that begins with a drive letter. 

                    

This parameter can contain any valid local file name. The file must be a properly registered file type, and the fax server must be able to access the file.


### -param JobParams [in]

Type: <b>PFAX_JOB_PARAM</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structure that contains the information necessary for the fax server to send the fax transmission. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and job scheduling information.


### -param CoverpageInfo [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> structure that contains personal data to display on the cover page of the fax document. This parameter must be <b>NULL</b> if a cover page is not required.


### -param FaxJobId [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive a unique number that identifies the queued job that will send the fax transmission.


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
One or all of the <i>FaxHandle</i>, <i>JobParams</i>, or <i>FileName</i> parameters are <b>NULL</b>; the call handle specified by the <b>CallHandle</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structure is invalid (should be <b>NULL</b>), or the <b>RecipientNumber</b> member in the <b>FAX_JOB_PARAM</b> structure is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter specifies a remote connection, but the <b>CallHandle</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structure is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">FAX_JOB_SUBMIT</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot locate the file specified by the <i>FileName</i> or the <i>CoverpageInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot process the file specified by the <i>FileName</i> or the <i>CoverpageInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to hand off a voice call to send a fax, using the <b>CallHandle</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structure. This functionality is not supported.

</td>
</tr>
</table>
 




## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/ms692819(v=VS.85).aspx">FaxCompleteJobParams</a> function before calling the FaxSendDocument function. <b>FaxCompleteJobParams</b> is a utility function that fills in multiple members in the <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> and <a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structures, with information such as the sender's name, the fax number, and optional billing code information.

The <b>FaxSendDocument</b> function executes asynchronously, and the function returns immediately. The fax server queues the job to send the fax transmission according to the details specified by the <a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structure.

For <b>FaxSendDocument</b> to succeed, there must be a remote fax printer installed on the fax server.

To send a fax document efficiently to multiple recipients, an application should call the <b>FaxSendDocument</b> function multiple times. The <a href="https://msdn.microsoft.com/en-us/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> function is supported for backward compatibility.

When you send a document from an application, links in the document may cause a dialog to appear, requesting information. If you do not handle the information request within several minutes, <b>FaxSendDocument</b> will fail and return an error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692819(v=VS.85).aspx">FaxCompleteJobParams</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a>
 

 

