---
UID: NF:comsvcs.ICrmCompensatorVariants.AbortRecordVariants
title: ICrmCompensatorVariants::AbortRecordVariants (comsvcs.h)
description: Delivers a log record to the CRM Compensator during the abort phase. (ICrmCompensatorVariants.AbortRecordVariants)
helpviewer_keywords: ["AbortRecordVariants","AbortRecordVariants method [COM+]","AbortRecordVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","AbortRecordVariants method","ICrmCompensatorVariants.AbortRecordVariants","ICrmCompensatorVariants::AbortRecordVariants","_dtc_ICrmCompensatorVariants_AbortRecordVariants","comsvcs/ICrmCompensatorVariants::AbortRecordVariants","cos.icrmcompensatorvariants_abortrecordvariants"]
old-location: cos\icrmcompensatorvariants_abortrecordvariants.htm
tech.root: cos
ms.assetid: a1ea366d-f3c6-4987-9f5b-32e3dd3e5d12
ms.date: 12/05/2018
ms.keywords: AbortRecordVariants, AbortRecordVariants method [COM+], AbortRecordVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],AbortRecordVariants method, ICrmCompensatorVariants.AbortRecordVariants, ICrmCompensatorVariants::AbortRecordVariants, _dtc_ICrmCompensatorVariants_AbortRecordVariants, comsvcs/ICrmCompensatorVariants::AbortRecordVariants, cos.icrmcompensatorvariants_abortrecordvariants
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
 - ICrmCompensatorVariants::AbortRecordVariants
 - comsvcs/ICrmCompensatorVariants::AbortRecordVariants
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
 - ICrmCompensatorVariants.AbortRecordVariants
---

# ICrmCompensatorVariants::AbortRecordVariants


## -description

Delivers a log record to the CRM Compensator during the abort phase.

## -parameters

### -param pLogRecord [in]

The log record (as a <b>Variant</b> array of <b>Variants</b>).

### -param pbForget [out]

Indicates whether the delivered record should be forgotten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method may be received by the CRM Compensator multiple times, once for each log record that is written. If no log records are written, the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-beginabortvariants">BeginAbortVariants</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-endabortvariants">EndAbortVariants</a> methods are received but there are no <b>AbortRecordVariants</b> method calls.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
