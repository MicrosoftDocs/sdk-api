---
UID: NF:faxcomex.IFaxOutgoingJob.get_SubmissionId
title: IFaxOutgoingJob::get_SubmissionId (faxcomex.h)
description: The IFaxOutgoingJob::get_SubmissionId property is a null-terminated string that contains the unique identifier assigned to the fax job during the submission process.
helpviewer_keywords: ["IFaxOutgoingJob interface [Fax Service]","SubmissionId property","IFaxOutgoingJob.SubmissionId","IFaxOutgoingJob.get_SubmissionId","IFaxOutgoingJob::SubmissionId","IFaxOutgoingJob::get_SubmissionId","SubmissionId property [Fax Service]","SubmissionId property [Fax Service]","IFaxOutgoingJob interface","_mfax_faxoutgoingjob.submissionid","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_submissionid_cpp","fax._mfax_faxoutgoingjob_submissionid","faxcomex/IFaxOutgoingJob::SubmissionId","faxcomex/IFaxOutgoingJob::get_SubmissionId","get_SubmissionId"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_submissionid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9btw.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob interface [Fax Service],SubmissionId property, IFaxOutgoingJob.SubmissionId, IFaxOutgoingJob.get_SubmissionId, IFaxOutgoingJob::SubmissionId, IFaxOutgoingJob::get_SubmissionId, SubmissionId property [Fax Service], SubmissionId property [Fax Service],IFaxOutgoingJob interface, _mfax_faxoutgoingjob.submissionid, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_submissionid_cpp, fax._mfax_faxoutgoingjob_submissionid, faxcomex/IFaxOutgoingJob::SubmissionId, faxcomex/IFaxOutgoingJob::get_SubmissionId, get_SubmissionId
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingJob::get_SubmissionId
 - faxcomex/IFaxOutgoingJob::get_SubmissionId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJob.SubmissionId
 - IFaxOutgoingJob.get_SubmissionId
 - IFaxOutgoingJob.get_SubmissionId
---

# IFaxOutgoingJob::get_SubmissionId


## -description

The <b>IFaxOutgoingJob::get_SubmissionId</b> property is a null-terminated string that contains the unique identifier assigned to the fax job during the submission process.

This property is read-only.

## -parameters

## -remarks

All fax jobs created by the same submission process share the same unique submission ID. When you submit a fax to be sent to more than one recipient, separate fax jobs will be created, but as part of the same fax broadcast, they will share the same <b>SubmissionID</b>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>