---
UID: NF:faxcom.IFaxJob.SetStatus
title: IFaxJob::SetStatus
author: windows-sdk-content
description: Call the IFaxJob::SetStatus method to pause, resume, cancel, or restart a specified fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_setstatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3d83.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxJob interface [Fax Service],SetStatus method, IFaxJob.SetStatus, IFaxJob::SetStatus, JC_DELETE, JC_PAUSE, JC_RESTART, JC_RESUME, SetStatus, SetStatus method [Fax Service], SetStatus method [Fax Service],IFaxJob interface, _mfax_ifaxjob_setstatus, fax._mfax_ifaxjob_mfax_ifaxjob_setstatus_cpp, fax._mfax_ifaxjob_setstatus, faxcom/IFaxJob::SetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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



You can use the <a href="https://msdn.microsoft.com/79fac214-78cf-4271-8c79-aa75a1661a48">IFaxJob::get_QueueStatus</a> property to retrieve the job queue status of a fax job.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/79fac214-78cf-4271-8c79-aa75a1661a48">IFaxJob::get_QueueStatus</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>



<a href="https://msdn.microsoft.com/7eb47777-cf5c-463d-bf19-5884c6fed04f">Managing Fax Jobs</a>
 

 

