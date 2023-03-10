---
UID: NS:bits5_0.__MIDL___MIDL_itf_bits5_0_0000_0000_0001
title: BITS_JOB_PROPERTY_VALUE
description: Provides the property value of the BITS job based on the value of the BITS_JOB_PROPERTY_ID enumeration.
helpviewer_keywords: ["BITS_JOB_PROPERTY_VALUE","BITS_JOB_PROPERTY_VALUE union [BITS]","bits.bits_job_property_value","bits.bits_job_property_value_union","bits5_0/BITS_JOB_PROPERTY_VALUE"]
old-location: bits\bits_job_property_value.htm
tech.root: Bits
ms.assetid: DF1DDB37-F16F-47FF-B6C1-8C545A827CCB
ms.date: 12/05/2018
ms.keywords: BITS_JOB_PROPERTY_VALUE, BITS_JOB_PROPERTY_VALUE union [BITS], bits.bits_job_property_value, bits.bits_job_property_value_union, bits5_0/BITS_JOB_PROPERTY_VALUE
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BITS_JOB_PROPERTY_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0001
 - bits5_0/__MIDL___MIDL_itf_bits5_0_0000_0000_0001
 - BITS_JOB_PROPERTY_VALUE
 - bits5_0/BITS_JOB_PROPERTY_VALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits5_0.h
api_name:
 - BITS_JOB_PROPERTY_VALUE
---

## -description

Provides the property value of the BITS job based on the value of the <a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_property_id">BITS_JOB_PROPERTY_ID</a> enumeration.

## -struct-fields

### -field Dword

This value is returned when using the enum property ID 
      <b>BITS_JOB_PROPERTY_ID_COST_FLAGS</b> and is applied as the 
      <a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_transfer_policy">transfer policy</a> on the BITS job.

This value is also used when using the <b>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</b> to specify the minimum notification interval.

### -field ClsID

This value is returned when using the enum property ID 
     <b>BITS_JOB_PROPERTY_NOTIFICATION_CLSID</b> and represents the CLSID of the callback object 
     to register with the BITS job.

### -field Enable

This value is returned when using the enum property ID 
     <b>BITS_JOB_PROPERTY_DYNAMIC_CONTENT</b> to specify whether the BITS job has dynamic 
      content. This value is also returned when using the enum property ID 
      <b>BITS_JOB_PROPERTY_HIGH_PERFORMANCE</b>  to specify whether to mark the BITS job as an optimized download.

This value is also used when using the <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b>  to specify whether the BITS job is in on demand or not.

### -field Uint64

This value is returned when using the enum property ID 
      <b>BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE</b> to represent the maximum allowed download size 
      of an optimized download.

### -field Target

This value is returned when using the enum property ID <b>BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS</b> to represent the intranet authentication target which is permitted to use stored credentials.

## -see-also

<a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_property_id">BITS_JOB_PROPERTY_ID</a>



<a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_transfer_policy">BITS_JOB_TRANSFER_POLICY</a>