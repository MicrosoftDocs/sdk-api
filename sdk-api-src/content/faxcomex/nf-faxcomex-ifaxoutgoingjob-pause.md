---
UID: NF:faxcomex.IFaxOutgoingJob.Pause
title: IFaxOutgoingJob::Pause (faxcomex.h)
description: The IFaxOutgoingJob::Pause method pauses the outbound fax job.
helpviewer_keywords: ["IFaxOutgoingJob interface [Fax Service]","Pause method","IFaxOutgoingJob.Pause","IFaxOutgoingJob::Pause","Pause","Pause method [Fax Service]","Pause method [Fax Service]","IFaxOutgoingJob interface","_mfax_faxoutgoingjob.pause","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_pause_cpp","fax._mfax_faxoutgoingjob_pause","faxcomex/IFaxOutgoingJob::Pause"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_pause_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7ijp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob interface [Fax Service],Pause method, IFaxOutgoingJob.Pause, IFaxOutgoingJob::Pause, Pause, Pause method [Fax Service], Pause method [Fax Service],IFaxOutgoingJob interface, _mfax_faxoutgoingjob.pause, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_pause_cpp, fax._mfax_faxoutgoingjob_pause, faxcomex/IFaxOutgoingJob::Pause
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
 - IFaxOutgoingJob::Pause
 - faxcomex/IFaxOutgoingJob::Pause
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
 - IFaxOutgoingJob.Pause
 - IFaxOutgoingJob.Pause
---

# IFaxOutgoingJob::Pause


## -description

The <b>IFaxOutgoingJob::Pause</b> method pauses the outbound fax job.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-resume-vb">IFaxOutgoingJob::Resume</a> method to resume a fax job after it has been paused.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farMANAGE_JOBS</b> access right. With the <b>farSUBMIT_LOW</b> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_JOBS</b> access right, users will be able to use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>
