---
UID: NF:comsvcs.ICrmCompensatorVariants.CommitRecordVariants
title: ICrmCompensatorVariants::CommitRecordVariants (comsvcs.h)
description: Delivers a log record to the CRM Compensator during the commit phase.
helpviewer_keywords: ["CommitRecordVariants","CommitRecordVariants method [COM+]","CommitRecordVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","CommitRecordVariants method","ICrmCompensatorVariants.CommitRecordVariants","ICrmCompensatorVariants::CommitRecordVariants","_dtc_ICrmCompensatorVariants_CommitRecordVariants","comsvcs/ICrmCompensatorVariants::CommitRecordVariants","cos.icrmcompensatorvariants_commitrecordvariants"]
old-location: cos\icrmcompensatorvariants_commitrecordvariants.htm
tech.root: cos
ms.assetid: 3d3ae282-d2cd-48cf-a093-c8f5ef9cc29a
ms.date: 12/05/2018
ms.keywords: CommitRecordVariants, CommitRecordVariants method [COM+], CommitRecordVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],CommitRecordVariants method, ICrmCompensatorVariants.CommitRecordVariants, ICrmCompensatorVariants::CommitRecordVariants, _dtc_ICrmCompensatorVariants_CommitRecordVariants, comsvcs/ICrmCompensatorVariants::CommitRecordVariants, cos.icrmcompensatorvariants_commitrecordvariants
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
 - ICrmCompensatorVariants::CommitRecordVariants
 - comsvcs/ICrmCompensatorVariants::CommitRecordVariants
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
 - ICrmCompensatorVariants.CommitRecordVariants
---

# ICrmCompensatorVariants::CommitRecordVariants


## -description

Delivers a log record to the CRM Compensator during the commit phase. Log records are delivered in the order in which they were written.

## -parameters

### -param pLogRecord [in]

The log record (as a Variant array of Variants).

### -param pbForget [out]

Indicates whether the delivered record should be forgotten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be received by the CRM Compensator multiple times, once for each log record that is written. If no log records are written, the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-begincommitvariants">BeginCommitVariants</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-endcommitvariants">EndCommitVariants</a> methods are received but there are no <b>CommitRecordVariants</b> method calls.

The CRM Compensator can choose to forget the record that is delivered to it during this method by setting the forget flag on return from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>