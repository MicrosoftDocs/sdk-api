---
UID: NF:faxcomex.IFaxDocument2.get_SubmissionId
title: IFaxDocument2::get_SubmissionId (faxcomex.h)
description: Retrieves the submission identifier for the fax document.
helpviewer_keywords: ["IFaxDocument2 interface [Fax Service]","SubmissionId property","IFaxDocument2.SubmissionId","IFaxDocument2.get_SubmissionId","IFaxDocument2::SubmissionId","IFaxDocument2::get_SubmissionId","SubmissionId property [Fax Service]","SubmissionId property [Fax Service]","IFaxDocument2 interface","_mfax_faxdocument2.submissionid","fax._mfax_faxdocument2_cpp_mfax_faxdocument2_submissionid_cpp","fax._mfax_faxdocument2_submissionid","faxcomex/IFaxDocument2::SubmissionId","faxcomex/IFaxDocument2::get_SubmissionId","get_SubmissionId"]
old-location: fax\_mfax_faxdocument2_cpp_mfax_faxdocument2_submissionid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\submissionid.htm
ms.date: 12/05/2018
ms.keywords: IFaxDocument2 interface [Fax Service],SubmissionId property, IFaxDocument2.SubmissionId, IFaxDocument2.get_SubmissionId, IFaxDocument2::SubmissionId, IFaxDocument2::get_SubmissionId, SubmissionId property [Fax Service], SubmissionId property [Fax Service],IFaxDocument2 interface, _mfax_faxdocument2.submissionid, fax._mfax_faxdocument2_cpp_mfax_faxdocument2_submissionid_cpp, fax._mfax_faxdocument2_submissionid, faxcomex/IFaxDocument2::SubmissionId, faxcomex/IFaxDocument2::get_SubmissionId, get_SubmissionId
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxDocument2::get_SubmissionId
 - faxcomex/IFaxDocument2::get_SubmissionId
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
 - IFaxDocument2.SubmissionId
 - IFaxDocument2.get_SubmissionId
 - IFaxDocument2.get_SubmissionId
---

# IFaxDocument2::get_SubmissionId


## -description

Retrieves the submission identifier for the fax document. Every job in a given broadcast receives the same submission identifier.


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read-only.

## -parameters

## -remarks

This property is set whenever a method that submits a fax completes.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument2">IFaxDocument2</a>