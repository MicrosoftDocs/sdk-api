---
UID: NF:winfax.FaxGetJobA
title: FaxGetJobA function (winfax.h)
author: windows-sdk-content
description: A fax client application calls the FaxGetJob function to retrieve detailed information for the specified queued or active fax job. The function returns the information in a FAX_JOB_ENTRY structure.
old-location: fax\_mfax_faxgetjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6jz6.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FaxGetJob, FaxGetJob function [Fax Service], FaxGetJobA, FaxGetJobW, _mfax_faxgetjob, fax._mfax_faxgetjob, winfax/FaxGetJob, winfax/FaxGetJobA, winfax/FaxGetJobW
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


A fax client application calls the <b>FaxGetJob</b> function to retrieve detailed information for the specified queued or active fax job. The function returns the information in a <a href="https://msdn.microsoft.com/en-us/library/ms690762(v=VS.85).aspx">FAX_JOB_ENTRY</a> structure.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies a queued or active fax job. The job can be an inbound or an outbound transmission.


### -param JobEntry [out]

Type: <b>PFAX_JOB_ENTRY*</b>

Pointer to the address of a buffer to receive a <a href="https://msdn.microsoft.com/en-us/library/ms690762(v=VS.85).aspx">FAX_JOB_ENTRY</a> structure. The data includes the job type and status, recipient and sender identification, scheduling and delivery settings, and the page count. For information about memory allocation, see the following Remarks section.


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
Access is denied. <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">FAX_JOB_QUERY</a> access is required.

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



The <b>FaxGetJob</b> function retrieves information about an individual fax job. To retrieve information about all queued and active jobs on the fax server of interest, call the <a href="https://msdn.microsoft.com/en-us/library/ms691958(v=VS.85).aspx">FaxEnumJobs</a> function.

The <b>FaxGetJob</b> function allocates the memory required for the buffer pointed to by the <i>JobEntry</i> parameter. An application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691821(v=VS.85).aspx">Managing Fax Jobs</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690762(v=VS.85).aspx">FAX_JOB_ENTRY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691958(v=VS.85).aspx">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691844(v=VS.85).aspx">FaxSetJob</a>
 

 

