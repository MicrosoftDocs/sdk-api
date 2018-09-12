---
UID: NF:winfax.FaxGetJobA
title: FaxGetJobA function
author: windows-sdk-content
description: A fax client application calls the FaxGetJob function to retrieve detailed information for the specified queued or active fax job. The function returns the information in a FAX_JOB_ENTRY structure.
old-location: fax\_mfax_faxgetjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6jz6.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxGetJob, FaxGetJob function [Fax Service], FaxGetJobA, FaxGetJobW, _mfax_faxgetjob, fax._mfax_faxgetjob, winfax/FaxGetJob, winfax/FaxGetJobA, winfax/FaxGetJobW
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
req.unicode-ansi: FaxGetJobW (Unicode) and FaxGetJobA (ANSI)
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
 - FaxGetJob
 - FaxGetJobA
 - FaxGetJobW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxGetJobA function


## -description


A fax client application calls the <b>FaxGetJob</b> function to retrieve detailed information for the specified queued or active fax job. The function returns the information in a <a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a> structure.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies a queued or active fax job. The job can be an inbound or an outbound transmission.


### -param JobEntry [out]

Type: <b>PFAX_JOB_ENTRY*</b>

Pointer to the address of a buffer to receive a <a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a> structure. The data includes the job type and status, recipient and sender identification, scheduling and delivery settings, and the page count. For information about memory allocation, see the following Remarks section.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_JOB_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>JobId</i> parameter is invalid, or one or both of the <i>JobEntry</i> or <i>FaxHandle</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
</table>
 




## -remarks



The <b>FaxGetJob</b> function retrieves information about an individual fax job. To retrieve information about all queued and active jobs on the fax server of interest, call the <a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a> function.

The <b>FaxGetJob</b> function allocates the memory required for the buffer pointed to by the <i>JobEntry</i> parameter. An application must call the <a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/7eb47777-cf5c-463d-bf19-5884c6fed04f">Managing Fax Jobs</a> and <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a>
 

 

