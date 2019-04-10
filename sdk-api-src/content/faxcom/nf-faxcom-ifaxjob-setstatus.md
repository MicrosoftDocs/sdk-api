---
UID: NF:faxcom.IFaxJob.SetStatus
title: IFaxJob::SetStatus (faxcom.h)
author: windows-sdk-content
description: Call the IFaxJob::SetStatus method to pause, resume, cancel, or restart a specified fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_setstatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3d83.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],SetStatus method, IFaxJob.SetStatus, IFaxJob::SetStatus, JC_DELETE, JC_PAUSE, JC_RESTART, JC_RESUME, SetStatus, SetStatus method [Fax Service], SetStatus method [Fax Service],IFaxJob interface, _mfax_ifaxjob_setstatus, fax._mfax_ifaxjob_mfax_ifaxjob_setstatus_cpp, fax._mfax_ifaxjob_setstatus, faxcom/IFaxJob::SetStatus
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
 - IFaxJob.SetStatus
 - IFaxJob.SetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::SetStatus


## -description


Call the <b>IFaxJob::SetStatus</b> method to pause, resume, cancel, or restart a specified fax job.


## -parameters




### -param Command [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the job command to perform. This parameter can be one of the following values.



#### JC_DELETE (JC_DELETE)

Cancel the specified fax job. The job can be active or queued.



#### JC_PAUSE (JC_PAUSE)

Pause the specified queued fax job. If the fax job is active, the fax service 
pauses the job when it returns to the queued state.



#### JC_RESUME (JC_RESUME)

Resume the paused fax job.



#### JC_RESTART (JC_RESTART)

Restart the specified fax job.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <a href="https://msdn.microsoft.com/en-us/library/ms692790(v=VS.85).aspx">IFaxJob::get_QueueStatus</a> property to retrieve the job queue status of a fax job.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692790(v=VS.85).aspx">IFaxJob::get_QueueStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691821(v=VS.85).aspx">Managing Fax Jobs</a>
 

 

