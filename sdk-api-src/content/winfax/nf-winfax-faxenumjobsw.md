---
UID: NF:winfax.FaxEnumJobsW
title: FaxEnumJobsW function (winfax.h)
description: The FaxEnumJobs function enumerates all queued and active fax jobs on the fax server to which the client has connected. The function returns detailed information for each fax job to the fax client application.helpviewer_keywords: ["FaxEnumJobs","FaxEnumJobs function [Fax Service]","FaxEnumJobsA","FaxEnumJobsW","_mfax_faxenumjobs","fax._mfax_faxenumjobs","winfax/FaxEnumJobs","winfax/FaxEnumJobsA","winfax/FaxEnumJobsW"]
old-location: fax\_mfax_faxenumjobs.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6fhv.htm
ms.date: 12/05/2018
ms.keywords: FaxEnumJobs, FaxEnumJobs function [Fax Service], FaxEnumJobsA, FaxEnumJobsW, _mfax_faxenumjobs, fax._mfax_faxenumjobs, winfax/FaxEnumJobs, winfax/FaxEnumJobsA, winfax/FaxEnumJobsW
f1_keywords:
- winfax/FaxEnumJobs
dev_langs:
- c++
req.header: winfax.h
req.include-header: 
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
- FaxEnumJobs
- FaxEnumJobsA
- FaxEnumJobsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FaxEnumJobsW function


## -description


The <b>FaxEnumJobs</b> function enumerates all queued and active fax jobs on the fax server to which the client has connected. The function returns detailed information for each fax job to the fax client application.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.


### -param JobEntry [out]

Type: <b>PFAX_JOB_ENTRY*</b>

Pointer to the address of a buffer to receive an array of <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_entrya">FAX_JOB_ENTRY</a> structures. Each structure describes one fax job. The data includes, among other items, the job type and status; recipient and sender identification; scheduling and delivery settings; and the page count. For information about memory allocation, see the following Remarks section.


### -param JobsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_entrya">FAX_JOB_ENTRY</a> structures the function returns in the <i>JobEntry</i> parameter.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

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
Access is denied. <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_JOB_QUERY</a> access is required.

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



The <b>FaxEnumJobs</b> function returns a list of fax jobs on the fax server of interest, as well as information available about each job. A fax administration application typically calls this function to display the fax job queue for administrative or query purposes. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-fax-jobs">Managing Fax Jobs</a>.

The <b>FaxEnumJobs</b> function allocates the memory required for the <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_entrya">FAX_JOB_ENTRY</a> buffer array pointed to by the <i>JobEntry</i> parameter. An application must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_entrya">FAX_JOB_ENTRY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetjoba">FaxGetJob</a>
 

 

