---
UID: NF:faxcom.IFaxJob.get_JobId
title: IFaxJob::get_JobId (faxcom.h)
description: The IFaxJob::get_JobId property is a number that uniquely identifies the specified fax job.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","JobId property","IFaxJob.JobId","IFaxJob.get_JobId","IFaxJob::JobId","IFaxJob::get_JobId","JobId property [Fax Service]","JobId property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_jobid","fax._mfax_ifaxjob_get_jobid","fax._mfax_ifaxjob_mfax_ifaxjob_get_jobid_cpp","faxcom/IFaxJob::JobId","faxcom/IFaxJob::get_JobId","get_JobId"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_jobid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0xwk.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],JobId property, IFaxJob.JobId, IFaxJob.get_JobId, IFaxJob::JobId, IFaxJob::get_JobId, JobId property [Fax Service], JobId property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_jobid, fax._mfax_ifaxjob_get_jobid, fax._mfax_ifaxjob_mfax_ifaxjob_get_jobid_cpp, faxcom/IFaxJob::JobId, faxcom/IFaxJob::get_JobId, get_JobId
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxJob::get_JobId
 - faxcom/IFaxJob::get_JobId
dev_langs:
 - c++
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
---

# IFaxJob::get_JobId


## -description

The <b>IFaxJob::get_JobId</b> property is a number that uniquely identifies the specified fax job.

This property is read-only.

## -parameters

## -remarks

You can use the <b>IFaxJob::get_JobId</b> property to uniquely identify a fax job because it is possible for multiple fax jobs to have the same <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-displayname-vb">IFaxJob::get_DisplayName</a> property. Note that the fax job identifier can be different from the identifier of a fax print job.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-displayname-vb">IFaxJob::get_DisplayName</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>