---
UID: NE:mfidl._MF_OPM_CGMSA_PROTECTION_LEVEL
title: MF_OPM_CGMSA_PROTECTION_LEVEL (mfidl.h)
description: Defines protection levels for MFPROTECTION_CGMSA.
helpviewer_keywords: ["MF_OPM_CGMSA_COPY_FREELY","MF_OPM_CGMSA_COPY_NEVER","MF_OPM_CGMSA_COPY_NO_MORE","MF_OPM_CGMSA_COPY_ONE_GENERATION","MF_OPM_CGMSA_OFF","MF_OPM_CGMSA_PROTECTION_LEVEL","MF_OPM_CGMSA_PROTECTION_LEVEL enumeration [Media Foundation]","MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED","mf.mf_opm_cgmsa_protection_level","mfidl/MF_OPM_CGMSA_COPY_FREELY","mfidl/MF_OPM_CGMSA_COPY_NEVER","mfidl/MF_OPM_CGMSA_COPY_NO_MORE","mfidl/MF_OPM_CGMSA_COPY_ONE_GENERATION","mfidl/MF_OPM_CGMSA_OFF","mfidl/MF_OPM_CGMSA_PROTECTION_LEVEL","mfidl/MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"]
old-location: mf\mf_opm_cgmsa_protection_level.htm
tech.root: mf
ms.assetid: EEFE04F7-E878-4F09-B973-B0FD3E9431AA
ms.date: 12/05/2018
ms.keywords: MF_OPM_CGMSA_COPY_FREELY, MF_OPM_CGMSA_COPY_NEVER, MF_OPM_CGMSA_COPY_NO_MORE, MF_OPM_CGMSA_COPY_ONE_GENERATION, MF_OPM_CGMSA_OFF, MF_OPM_CGMSA_PROTECTION_LEVEL, MF_OPM_CGMSA_PROTECTION_LEVEL enumeration [Media Foundation], MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED, mf.mf_opm_cgmsa_protection_level, mfidl/MF_OPM_CGMSA_COPY_FREELY, mfidl/MF_OPM_CGMSA_COPY_NEVER, mfidl/MF_OPM_CGMSA_COPY_NO_MORE, mfidl/MF_OPM_CGMSA_COPY_ONE_GENERATION, mfidl/MF_OPM_CGMSA_OFF, mfidl/MF_OPM_CGMSA_PROTECTION_LEVEL, mfidl/MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MF_OPM_CGMSA_PROTECTION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_OPM_CGMSA_PROTECTION_LEVEL
 - mfidl/_MF_OPM_CGMSA_PROTECTION_LEVEL
 - MF_OPM_CGMSA_PROTECTION_LEVEL
 - mfidl/MF_OPM_CGMSA_PROTECTION_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_OPM_CGMSA_PROTECTION_LEVEL
---

# MF_OPM_CGMSA_PROTECTION_LEVEL enumeration


## -description

Defines protection levels for <b>MFPROTECTION_CGMSA</b>.

## -enum-fields

### -field MF_OPM_CGMSA_OFF:0

CGMS-A is disabled.

### -field MF_OPM_CGMSA_COPY_FREELY:0x1

The protection level is Copy Freely.

### -field MF_OPM_CGMSA_COPY_NO_MORE:0x2

The protection level is Copy No More.

### -field MF_OPM_CGMSA_COPY_ONE_GENERATION:0x3

The protection level is Copy One Generation.

### -field MF_OPM_CGMSA_COPY_NEVER:0x4

The protection level is Copy Never.

### -field MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED:0x8

Redistribution control (also called the broadcast flag) is required. This flag can be combined with the other flags.

## -remarks

These flags are equivalent to the OPM_CGMSA_Protection_Level enumeration constants used in the Output Protection Protocol (OPM).

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
