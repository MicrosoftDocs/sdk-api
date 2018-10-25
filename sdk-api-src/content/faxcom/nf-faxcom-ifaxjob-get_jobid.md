---
UID: NF:faxcom.IFaxJob.get_JobId
title: IFaxJob::get_JobId
author: windows-sdk-content
description: The IFaxJob::get_JobId property is a number that uniquely identifies the specified fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_jobid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0xwk.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxJob interface [Fax Service],JobId property, IFaxJob.JobId, IFaxJob.get_JobId, IFaxJob::JobId, IFaxJob::get_JobId, JobId property [Fax Service], JobId property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_jobid, fax._mfax_ifaxjob_get_jobid, fax._mfax_ifaxjob_mfax_ifaxjob_get_jobid_cpp, faxcom/IFaxJob::JobId, faxcom/IFaxJob::get_JobId, get_JobId
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
 - IFaxJob.JobId
 - IFaxJob.get_JobId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_JobId


## -description


The <b>IFaxJob::get_JobId</b> property is a number that uniquely identifies the specified fax job.

This property is read-only.


## -parameters


## -remarks



You can use the <b>IFaxJob::get_JobId</b> property to uniquely identify a fax job because it is possible for multiple fax jobs to have the same <a href="https://msdn.microsoft.com/45ba0af1-25cc-4020-ae5c-355e318a63bf">IFaxJob::get_DisplayName</a> property. Note that the fax job identifier can be different from the identifier of a fax print job.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/45ba0af1-25cc-4020-ae5c-355e318a63bf">IFaxJob::get_DisplayName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

