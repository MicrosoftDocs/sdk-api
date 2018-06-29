---
UID: NF:faxcom.IFaxJob.get_JobId
title: IFaxJob::get_JobId
author: windows-sdk-content
description: The JobId property is a number that uniquely identifies the specified fax job.
old-location: fax\_mfax_ifaxjob_get_jobid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0xwk.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
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



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

