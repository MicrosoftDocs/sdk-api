---
UID: NF:comsvcs.ICrmCompensator.PrepareRecord
title: ICrmCompensator::PrepareRecord (comsvcs.h)
description: Delivers a log record in forward order during the prepare phase.
helpviewer_keywords: ["ICrmCompensator interface [COM+]","PrepareRecord method","ICrmCompensator.PrepareRecord","ICrmCompensator::PrepareRecord","PrepareRecord","PrepareRecord method [COM+]","PrepareRecord method [COM+]","ICrmCompensator interface","_dtc_ICrmCompensator_PrepareRecord","comsvcs/ICrmCompensator::PrepareRecord","cos.icrmcompensator_preparerecord"]
old-location: cos\icrmcompensator_preparerecord.htm
tech.root: cos
ms.assetid: 12b4d0d5-29f3-4fbb-8091-1b7d5ba0adb4
ms.date: 12/05/2018
ms.keywords: ICrmCompensator interface [COM+],PrepareRecord method, ICrmCompensator.PrepareRecord, ICrmCompensator::PrepareRecord, PrepareRecord, PrepareRecord method [COM+], PrepareRecord method [COM+],ICrmCompensator interface, _dtc_ICrmCompensator_PrepareRecord, comsvcs/ICrmCompensator::PrepareRecord, cos.icrmcompensator_preparerecord
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
 - ICrmCompensator::PrepareRecord
 - comsvcs/ICrmCompensator::PrepareRecord
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
 - ICrmCompensator.PrepareRecord
---

# ICrmCompensator::PrepareRecord


## -description

Delivers a log record in forward order during the prepare phase. This method can be received by the CRM Compensator multiple times, once for each log record that is written.

## -parameters

### -param crmLogRec [in]

The log record, as a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-crmlogrecordread">CrmLogRecordRead</a> structure.

### -param pfForget [out]

Indicates whether the delivered record should be forgotten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Unstructured log records are delivered as a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-crmlogrecordread">CrmLogRecordRead</a> structure. In addition to the user data (as a single BLOB), this structure contains a couple of additional fields that might be useful for debugging or fault-finding if human compensation is necessary. The <b>dwCrmFlags</b> member is a bitfield that provides further information about whether this record was forgotten at some point and when it was written. The <b>dwSequenceNumber</b> member provides the sequence number of the log record. In most cases, sequence numbers are sequential but are not necessarily contiguous due to internal log records that are not delivered to the CRM Compensator.

If no log records are written by the CRM Worker, the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-beginprepare">BeginPrepare</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-endprepare">EndPrepare</a> methods are received but there are no <b>PrepareRecord</b> method calls. This is to allow for CRM Compensators that write log records at prepare time only.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>