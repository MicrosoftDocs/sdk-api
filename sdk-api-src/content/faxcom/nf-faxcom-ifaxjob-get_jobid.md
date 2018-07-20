---
UID: NF:faxcom.IFaxJob.get_JobId
title: IFaxJob::get_JobId
author: windows-sdk-content
description: The JobId property is a number that uniquely identifies the specified fax job.
old-location: fax\_mfax_ifaxjob_get_jobid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0xwk.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FaxJob object [Fax Service],JobId property, FaxJob.JobId, IFaxJob.get_JobId, IFaxJob::get_JobId, JobId property [Fax Service], JobId property [Fax Service],FaxJob object, _mfax_ifaxjob_get_jobid, fax._mfax_ifaxjob_get_jobid, fax._mfax_ifaxjob_get_jobid_vb, get_JobId
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
 - FaxJob.JobId
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_JobId


## -description


The <b>JobId</b> property is a number that uniquely identifies the specified fax job.

This property is read-only.


## -parameters


## -remarks



You can use the <b>JobId</b> property to uniquely identify a fax job because it is possible for multiple fax jobs to have the same <a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a> property. Note that the fax job identifier can be different from the identifier of a fax print job.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c6e95bae-c1f8-4636-9847-7c66187cfc8d">FaxJob</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>
 

 

