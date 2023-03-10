---
UID: NF:comsvcs.ICrmCompensatorVariants.PrepareRecordVariants
title: ICrmCompensatorVariants::PrepareRecordVariants (comsvcs.h)
description: Delivers a log record to the CRM Compensator during the prepare phase.
helpviewer_keywords: ["ICrmCompensatorVariants interface [COM+]","PrepareRecordVariants method","ICrmCompensatorVariants.PrepareRecordVariants","ICrmCompensatorVariants::PrepareRecordVariants","PrepareRecordVariants","PrepareRecordVariants method [COM+]","PrepareRecordVariants method [COM+]","ICrmCompensatorVariants interface","_dtc_ICrmCompensatorVariants_PrepareRecordVariants","comsvcs/ICrmCompensatorVariants::PrepareRecordVariants","cos.icrmcompensatorvariants_preparerecordvariants"]
old-location: cos\icrmcompensatorvariants_preparerecordvariants.htm
tech.root: cos
ms.assetid: 5cbe3bf9-b82c-42da-ac19-dddb5837368e
ms.date: 12/05/2018
ms.keywords: ICrmCompensatorVariants interface [COM+],PrepareRecordVariants method, ICrmCompensatorVariants.PrepareRecordVariants, ICrmCompensatorVariants::PrepareRecordVariants, PrepareRecordVariants, PrepareRecordVariants method [COM+], PrepareRecordVariants method [COM+],ICrmCompensatorVariants interface, _dtc_ICrmCompensatorVariants_PrepareRecordVariants, comsvcs/ICrmCompensatorVariants::PrepareRecordVariants, cos.icrmcompensatorvariants_preparerecordvariants
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
 - ICrmCompensatorVariants::PrepareRecordVariants
 - comsvcs/ICrmCompensatorVariants::PrepareRecordVariants
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
 - ICrmCompensatorVariants.PrepareRecordVariants
---

# ICrmCompensatorVariants::PrepareRecordVariants


## -description

Delivers a log record to the CRM Compensator during the prepare phase. Log records are delivered in the order in which they were written.

## -parameters

### -param pLogRecord [in]

The log record (as a <b>Variant</b> array of <b>Variants</b>).

### -param pbForget [out]

Indicates whether the delivered record should be forgotten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be received by the CRM Compensator multiple times, once for each log record that is written.

For the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a> interface, log records are delivered in the same way that they were written. The CRM flags and sequence number are appended as the last two elements in the array. (See <b>ICrmCompensator::PrepareRecord</b>.)

If no log records are written by the CRM Worker, the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-beginpreparevariants">BeginPrepareVariants</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-endpreparevariants">EndPrepareVariants</a> methods are received by the CRM Compensator but there are no <b>PrepareRecordVariants</b> method calls. This is to allow for CRM Compensators that write log records at prepare time only.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>