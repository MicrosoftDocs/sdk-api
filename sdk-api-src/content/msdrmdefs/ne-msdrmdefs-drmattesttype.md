---
UID: NE:msdrmdefs._DRMATTESTTYPE
title: DRMATTESTTYPE (msdrmdefs.h)
description: The DRMATTESTTYPE enumeration specifies what kind of signature to create for a data blob.
helpviewer_keywords: ["DRMATTESTTYPE","DRMATTESTTYPE enumeration [Active Directory Rights Management Services SDK 1.0]","DRMATTESTTYPE_FULLENVIRONMENT","DRMATTESTTYPE_HASHONLY","msdrmdefs/DRMATTESTTYPE","msdrmdefs/DRMATTESTTYPE_FULLENVIRONMENT","msdrmdefs/DRMATTESTTYPE_HASHONLY","rm.drmattesttype"]
old-location: rm\drmattesttype.htm
tech.root: rm
ms.assetid: adbf8718-e707-4ab9-a961-f8b4b4e1fe6a
ms.date: 12/05/2018
ms.keywords: DRMATTESTTYPE, DRMATTESTTYPE enumeration [Active Directory Rights Management Services SDK 1.0], DRMATTESTTYPE_FULLENVIRONMENT, DRMATTESTTYPE_HASHONLY, msdrmdefs/DRMATTESTTYPE, msdrmdefs/DRMATTESTTYPE_FULLENVIRONMENT, msdrmdefs/DRMATTESTTYPE_HASHONLY, rm.drmattesttype
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
req.typenames: DRMATTESTTYPE
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRMATTESTTYPE
 - msdrmdefs/_DRMATTESTTYPE
 - DRMATTESTTYPE
 - msdrmdefs/DRMATTESTTYPE
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
 - DRMATTESTTYPE
---

# DRMATTESTTYPE enumeration


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRMATTESTTYPE</b> enumeration specifies what kind of signature to create for a data blob.

## -enum-fields

### -field DRMATTESTTYPE_FULLENVIRONMENT

Create a signature using full environment information.

### -field DRMATTESTTYPE_HASHONLY

Create a signature using only a hash of the environment.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmattest">DRMAttest</a>