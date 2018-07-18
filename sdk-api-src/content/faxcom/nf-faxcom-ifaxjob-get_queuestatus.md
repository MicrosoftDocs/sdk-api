---
UID: NF:faxcom.IFaxJob.get_QueueStatus
title: IFaxJob::get_QueueStatus
author: windows-sdk-content
description: The QueueStatus property is a null-terminated string that describes the job queue status of the fax job.
old-location: fax\_mfax_ifaxjob_get_queuestatus_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8mnn.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: Deleting, Failed, FaxJob object [Fax Service],QueueStatus property, FaxJob.QueueStatus, IFaxJob.get_QueueStatus, IFaxJob::get_QueueStatus, In Progress, No Line, Paused, Pending, QueueStatus property [Fax Service], QueueStatus property [Fax Service],FaxJob object, Retries Exceeded, Retrying, _mfax_ifaxjob_get_queuestatus, fax._mfax_ifaxjob_get_queuestatus, fax._mfax_ifaxjob_get_queuestatus_vb, get_QueueStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxJob.QueueStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_QueueStatus


## -description


The <b>QueueStatus</b> property is a null-terminated string that describes the job queue status of the fax job.

This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <b>Deleting</b>, <b>Failed</b>, <b>Paused</b>, <b>No Line</b>, <b>Retrying</b>, and <b>Retries Exceeded</b> values are supported only in Windows XP with Service Pack 1 installed, and in Windows Server 2003.</div>
<div> </div>
<b>QueueStatus</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

