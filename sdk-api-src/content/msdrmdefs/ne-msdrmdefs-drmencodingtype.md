---
UID: NE:msdrmdefs._DRMENCODINGTYPE
title: DRMENCODINGTYPE (msdrmdefs.h)
description: The DRMENCODINGTYPE enumeration identifies possible encoding types used in licenses.
helpviewer_keywords: ["DRMENCODINGTYPE","DRMENCODINGTYPE enumeration [Active Directory Rights Management Services SDK 1.0]","DRMENCODINGTYPE_BASE64","DRMENCODINGTYPE_LONG","DRMENCODINGTYPE_RAW","DRMENCODINGTYPE_STRING","DRMENCODINGTYPE_TIME","DRMENCODINGTYPE_UINT","msdrmdefs/DRMENCODINGTYPE","msdrmdefs/DRMENCODINGTYPE_BASE64","msdrmdefs/DRMENCODINGTYPE_LONG","msdrmdefs/DRMENCODINGTYPE_RAW","msdrmdefs/DRMENCODINGTYPE_STRING","msdrmdefs/DRMENCODINGTYPE_TIME","msdrmdefs/DRMENCODINGTYPE_UINT","rm.drmencodingtype"]
old-location: rm\drmencodingtype.htm
tech.root: rm
ms.assetid: 7859d7e9-aec4-4255-a11b-5d18c08fd6ca
ms.date: 12/05/2018
ms.keywords: DRMENCODINGTYPE, DRMENCODINGTYPE enumeration [Active Directory Rights Management Services SDK 1.0], DRMENCODINGTYPE_BASE64, DRMENCODINGTYPE_LONG, DRMENCODINGTYPE_RAW, DRMENCODINGTYPE_STRING, DRMENCODINGTYPE_TIME, DRMENCODINGTYPE_UINT, msdrmdefs/DRMENCODINGTYPE, msdrmdefs/DRMENCODINGTYPE_BASE64, msdrmdefs/DRMENCODINGTYPE_LONG, msdrmdefs/DRMENCODINGTYPE_RAW, msdrmdefs/DRMENCODINGTYPE_STRING, msdrmdefs/DRMENCODINGTYPE_TIME, msdrmdefs/DRMENCODINGTYPE_UINT, rm.drmencodingtype
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DRMENCODINGTYPE
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRMENCODINGTYPE
 - msdrmdefs/_DRMENCODINGTYPE
 - DRMENCODINGTYPE
 - msdrmdefs/DRMENCODINGTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRMENCODINGTYPE
---

# DRMENCODINGTYPE enumeration


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRMENCODINGTYPE</b> enumeration identifies possible encoding types used in licenses.

## -enum-fields

### -field DRMENCODINGTYPE_BASE64

Base 64 encoded value.

### -field DRMENCODINGTYPE_STRING

String value.

### -field DRMENCODINGTYPE_LONG

Long value.

### -field DRMENCODINGTYPE_TIME

Time value.

### -field DRMENCODINGTYPE_UINT

Unsigned integer.

### -field DRMENCODINGTYPE_RAW

Binary data.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>