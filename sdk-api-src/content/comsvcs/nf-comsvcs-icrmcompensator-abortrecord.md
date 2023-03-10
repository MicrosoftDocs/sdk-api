---
UID: NF:comsvcs.ICrmCompensator.AbortRecord
title: ICrmCompensator::AbortRecord (comsvcs.h)
description: Delivers a log record to the CRM Compensator during the abort phase. (ICrmCompensator.AbortRecord)
helpviewer_keywords: ["AbortRecord","AbortRecord method [COM+]","AbortRecord method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","AbortRecord method","ICrmCompensator.AbortRecord","ICrmCompensator::AbortRecord","_dtc_ICrmCompensator_AbortRecord","comsvcs/ICrmCompensator::AbortRecord","cos.icrmcompensator_abortrecord"]
old-location: cos\icrmcompensator_abortrecord.htm
tech.root: cos
ms.assetid: 79dcf391-7ec9-4c9c-9f91-0e806d7c278c
ms.date: 12/05/2018
ms.keywords: AbortRecord, AbortRecord method [COM+], AbortRecord method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],AbortRecord method, ICrmCompensator.AbortRecord, ICrmCompensator::AbortRecord, _dtc_ICrmCompensator_AbortRecord, comsvcs/ICrmCompensator::AbortRecord, cos.icrmcompensator_abortrecord
req.header: comsvcs.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmCompensator::AbortRecord
 - comsvcs/ICrmCompensator::AbortRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmCompensator.AbortRecord
---

# ICrmCompensator::AbortRecord


## -description

Delivers a log record to the CRM Compensator during the abort phase.

## -parameters

### -param crmLogRec [in]

The log record, as a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-crmlogrecordread">CrmLogRecordRead</a> structure.

### -param pfForget [out]

Indicates whether the delivered record should be forgotten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Log records are delivered in the reverse order in which they were written. This method can be received by the CRM Compensator multiple times, once for each log record that was written. If no log records are written, the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-beginabort">BeginAbort</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-endabort">EndAbort</a> methods are received but there are no <b>AbortRecord</b> method calls.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
