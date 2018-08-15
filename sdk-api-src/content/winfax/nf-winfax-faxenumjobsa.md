---
UID: NF:winfax.FaxEnumJobsA
title: FaxEnumJobsA function
author: windows-sdk-content
description: The FaxEnumJobs function enumerates all queued and active fax jobs on the fax server to which the client has connected. The function returns detailed information for each fax job to the fax client application.
old-location: fax\_mfax_faxenumjobs.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6fhv.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxEnumJobs, FaxEnumJobs function [Fax Service], FaxEnumJobsA, FaxEnumJobsW, _mfax_faxenumjobs, fax._mfax_faxenumjobs, winfax/FaxEnumJobs, winfax/FaxEnumJobsA, winfax/FaxEnumJobsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winfax.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxEnumJobsW (Unicode) and FaxEnumJobsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxEnumJobs
 - FaxEnumJobsA
 - FaxEnumJobsW
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxEnumJobsA function


## -description


The <b>FaxEnumJobs</b> function enumerates all queued and active fax jobs on the fax server to which the client has connected. The function returns detailed information for each fax job to the fax client application.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param JobEntry [out]

Type: <b>PFAX_JOB_ENTRY*</b>

Pointer to the address of a buffer to receive an array of <a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a> structures. Each structure describes one fax job. The data includes, among other items, the job type and status; recipient and sender identification; scheduling and delivery settings; and the page count. For information about memory allocation, see the following Remarks section.


### -param JobsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a> structures the function returns in the <i>JobEntry</i> parameter.


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
One or all of the <i>JobsReturned</i>, <i>JobEntry</i>, or <i>FaxHandle</i> parameters are <b>NULL</b>.

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



The <b>FaxEnumJobs</b> function returns a list of fax jobs on the fax server of interest, as well as information available about each job. A fax administration application typically calls this function to display the fax job queue for administrative or query purposes. For more information, see <a href="https://msdn.microsoft.com/7eb47777-cf5c-463d-bf19-5884c6fed04f">Managing Fax Jobs</a>.

The <b>FaxEnumJobs</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a> buffer array pointed to by the <i>JobEntry</i> parameter. An application must call the <a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/784c4945-b4cc-446b-b0d4-c2fc58d46a9d">FaxGetJob</a>
 

 

