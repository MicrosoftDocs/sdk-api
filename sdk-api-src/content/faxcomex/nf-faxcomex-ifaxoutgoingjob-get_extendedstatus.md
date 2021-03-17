---
UID: NF:faxcomex.IFaxOutgoingJob.get_ExtendedStatus
title: IFaxOutgoingJob::get_ExtendedStatus (faxcomex.h)
description: The IFaxOutgoingJob::get_ExtendedStatus property is a null-terminated string that describes the job's extended status.
helpviewer_keywords: ["ExtendedStatus property [Fax Service]","ExtendedStatus property [Fax Service]","IFaxOutgoingJob interface","IFaxOutgoingJob interface [Fax Service]","ExtendedStatus property","IFaxOutgoingJob.ExtendedStatus","IFaxOutgoingJob.get_ExtendedStatus","IFaxOutgoingJob::ExtendedStatus","IFaxOutgoingJob::get_ExtendedStatus","_mfax_faxoutgoingjob.extendedstatus","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_extendedstatus_cpp","fax._mfax_faxoutgoingjob_extendedstatus","faxcomex/IFaxOutgoingJob::ExtendedStatus","faxcomex/IFaxOutgoingJob::get_ExtendedStatus","get_ExtendedStatus"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_extendedstatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_36er.htm
ms.date: 12/05/2018
ms.keywords: ExtendedStatus property [Fax Service], ExtendedStatus property [Fax Service],IFaxOutgoingJob interface, IFaxOutgoingJob interface [Fax Service],ExtendedStatus property, IFaxOutgoingJob.ExtendedStatus, IFaxOutgoingJob.get_ExtendedStatus, IFaxOutgoingJob::ExtendedStatus, IFaxOutgoingJob::get_ExtendedStatus, _mfax_faxoutgoingjob.extendedstatus, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_extendedstatus_cpp, fax._mfax_faxoutgoingjob_extendedstatus, faxcomex/IFaxOutgoingJob::ExtendedStatus, faxcomex/IFaxOutgoingJob::get_ExtendedStatus, get_ExtendedStatus
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
 - IFaxOutgoingJob::get_ExtendedStatus
 - faxcomex/IFaxOutgoingJob::get_ExtendedStatus
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
 - IFaxOutgoingJob.ExtendedStatus
 - IFaxOutgoingJob.get_ExtendedStatus
 - IFaxOutgoingJob.get_ExtendedStatus
---

# IFaxOutgoingJob::get_ExtendedStatus


## -description

The <b>IFaxOutgoingJob::get_ExtendedStatus</b> property is a null-terminated string that describes the job's extended status.

This property is read-only.

## -parameters

## -remarks

The <b>IFaxOutgoingJob::get_ExtendedStatus</b> property can have a value only if the fax service provider (FSP) returns a proprietary status code in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatuscode-vb">IFaxOutgoingJob::get_ExtendedStatusCode</a> property. Otherwise, the <b>IFaxOutgoingJob::get_ExtendedStatus</b> property will contain an empty string. Similarly, an FSP may choose not to provide values for the <b>IFaxOutgoingJob::get_ExtendedStatus</b> property, and the property will thus contain an empty string. This is the case for the T.30 FSP provided with the fax service.

If an FSP provides a proprietary status code, the service loads the code string from the FSP, and passes both the string and the original status code to the client. If the FSP provides a status defined in <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_extended_status_enum">FAX_JOB_EXTENDED_STATUS_ENUM</a>, the service passes only the status code to the client.

A fax client application should check the extended status string first. If the string is not <b>NULL</b>/empty, it describes the extended status, and the extended status code is the same code that the FSP passed to the fax service. If the string is <b>NULL</b>/empty, the extended status code is one of those defined in <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_extended_status_enum">FAX_JOB_EXTENDED_STATUS_ENUM</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>