---
UID: NS:comsvcs.tagCrmLogRecordRead
title: CrmLogRecordRead (comsvcs.h)
description: Contains unstructured log records for the Compensating Resource Manager (CRM).
helpviewer_keywords: ["CrmLogRecordRead","CrmLogRecordRead structure [COM+]","_cos_CrmLogRecordRead","comsvcs/CrmLogRecordRead","cos.crmlogrecordread"]
old-location: cos\crmlogrecordread.htm
tech.root: cos
ms.assetid: 0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6
ms.date: 12/05/2018
ms.keywords: CrmLogRecordRead, CrmLogRecordRead structure [COM+], _cos_CrmLogRecordRead, comsvcs/CrmLogRecordRead, cos.crmlogrecordread
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
req.typenames: CrmLogRecordRead
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCrmLogRecordRead
 - comsvcs/tagCrmLogRecordRead
 - CrmLogRecordRead
 - comsvcs/CrmLogRecordRead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CrmLogRecordRead
---

# CrmLogRecordRead structure


## -description

Contains unstructured log records for the Compensating Resource Manager (CRM).

## -struct-fields

### -field dwCrmFlags

Information about when this record was written. For a list of values, see <a href="/windows/desktop/api/comsvcs/ne-comsvcs-crmflags">CRMFLAGS</a>.

### -field dwSequenceNumber

The sequence number of the log record. Sequence numbers are not necessarily contiguous because not all internal log records or forgotten log records are delivered to the CRM Compensator.

### -field blobUserData

The user data.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmformatlogrecords">ICrmFormatLogRecords</a>