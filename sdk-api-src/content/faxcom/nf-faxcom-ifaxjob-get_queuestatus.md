---
UID: NF:faxcom.IFaxJob.get_QueueStatus
title: IFaxJob::get_QueueStatus (faxcom.h)
author: windows-sdk-content
description: The IFaxJob::get_QueueStatus property is a null-terminated string that describes the job queue status of the fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_queuestatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8mnn.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Deleting, Failed, IFaxJob interface [Fax Service],QueueStatus property, IFaxJob.QueueStatus, IFaxJob.get_QueueStatus, IFaxJob::QueueStatus, IFaxJob::get_QueueStatus, In Progress, No Line, Paused, Pending, QueueStatus property [Fax Service], QueueStatus property [Fax Service],IFaxJob interface, Retries Exceeded, Retrying, _mfax_ifaxjob_get_queuestatus, fax._mfax_ifaxjob_get_queuestatus, fax._mfax_ifaxjob_mfax_ifaxjob_get_queuestatus_cpp, faxcom/IFaxJob::QueueStatus, faxcom/IFaxJob::get_QueueStatus, get_QueueStatus
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxJob.QueueStatus
 - IFaxJob.get_QueueStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxJob::get_QueueStatus


## -description


The <b>IFaxJob::get_QueueStatus</b> property is a null-terminated string that describes the job queue status of the fax job.

This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <b>Deleting</b>, <b>Failed</b>, <b>Paused</b>, <b>No Line</b>, <b>Retrying</b>, and <b>Retries Exceeded</b> values are supported only in Windows XP with Service Pack 1 installed, and in Windows Server 2003.</div>
<div> </div>
<b>IFaxJob::get_QueueStatus</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

