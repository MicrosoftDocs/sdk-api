---
UID: NE:msdrmdefs._DRMTIMETYPE
title: DRMTIMETYPE (msdrmdefs.h)
description: The DRMTIMETYPE enumeration specifies a time type.
helpviewer_keywords: ["DRMTIMETYPE","DRMTIMETYPE enumeration [Active Directory Rights Management Services SDK 1.0]","DRMTIMETYPE_SYSTEMLOCAL","DRMTIMETYPE_SYSTEMUTC","msdrmdefs/DRMTIMETYPE","msdrmdefs/DRMTIMETYPE_SYSTEMLOCAL","msdrmdefs/DRMTIMETYPE_SYSTEMUTC","rm.drmtimetype"]
old-location: rm\drmtimetype.htm
tech.root: rm
ms.assetid: 0adb6824-0b6e-414a-b9d2-a3266c80df23
ms.date: 12/05/2018
ms.keywords: DRMTIMETYPE, DRMTIMETYPE enumeration [Active Directory Rights Management Services SDK 1.0], DRMTIMETYPE_SYSTEMLOCAL, DRMTIMETYPE_SYSTEMUTC, msdrmdefs/DRMTIMETYPE, msdrmdefs/DRMTIMETYPE_SYSTEMLOCAL, msdrmdefs/DRMTIMETYPE_SYSTEMUTC, rm.drmtimetype
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
req.typenames: DRMTIMETYPE
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRMTIMETYPE
 - msdrmdefs/_DRMTIMETYPE
 - DRMTIMETYPE
 - msdrmdefs/DRMTIMETYPE
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
 - DRMTIMETYPE
---

# DRMTIMETYPE enumeration


## -description

> [!NOTE] 
> The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRMTIMETYPE</b> enumeration specifies a time type.

## -enum-fields

### -field DRMTIMETYPE_SYSTEMUTC

Greenwich Mean Time (Universal Time).

### -field DRMTIMETYPE_SYSTEMLOCAL

Local time.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>