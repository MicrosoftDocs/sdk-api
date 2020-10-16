---
UID: NE:msdrmdefs._DRM_USAGEPOLICY_TYPE
title: DRM_USAGEPOLICY_TYPE (msdrmdefs.h)
description: Used with the DRMGetUsagePolicy and DRMSetUsagePolicy functions to specify a type of usage policy.
helpviewer_keywords: ["DRM_USAGEPOLICY_TYPE","DRM_USAGEPOLICY_TYPE enumeration [Active Directory Rights Management Services SDK 1.0]","DRM_USAGEPOLICY_TYPE_BYDIGEST","DRM_USAGEPOLICY_TYPE_BYNAME","DRM_USAGEPOLICY_TYPE_BYPUBLICKEY","DRM_USAGEPOLICY_TYPE_OSEXCLUSION","msdrmdefs/DRM_USAGEPOLICY_TYPE","msdrmdefs/DRM_USAGEPOLICY_TYPE_BYDIGEST","msdrmdefs/DRM_USAGEPOLICY_TYPE_BYNAME","msdrmdefs/DRM_USAGEPOLICY_TYPE_BYPUBLICKEY","msdrmdefs/DRM_USAGEPOLICY_TYPE_OSEXCLUSION","rm.drm_usagepolicy_type"]
old-location: rm\drm_usagepolicy_type.htm
tech.root: rm
ms.assetid: b7486f70-36da-4868-9b50-caa37f7a7539
ms.date: 12/05/2018
ms.keywords: DRM_USAGEPOLICY_TYPE, DRM_USAGEPOLICY_TYPE enumeration [Active Directory Rights Management Services SDK 1.0], DRM_USAGEPOLICY_TYPE_BYDIGEST, DRM_USAGEPOLICY_TYPE_BYNAME, DRM_USAGEPOLICY_TYPE_BYPUBLICKEY, DRM_USAGEPOLICY_TYPE_OSEXCLUSION, msdrmdefs/DRM_USAGEPOLICY_TYPE, msdrmdefs/DRM_USAGEPOLICY_TYPE_BYDIGEST, msdrmdefs/DRM_USAGEPOLICY_TYPE_BYNAME, msdrmdefs/DRM_USAGEPOLICY_TYPE_BYPUBLICKEY, msdrmdefs/DRM_USAGEPOLICY_TYPE_OSEXCLUSION, rm.drm_usagepolicy_type
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
req.typenames: DRM_USAGEPOLICY_TYPE
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRM_USAGEPOLICY_TYPE
 - msdrmdefs/_DRM_USAGEPOLICY_TYPE
 - DRM_USAGEPOLICY_TYPE
 - msdrmdefs/DRM_USAGEPOLICY_TYPE
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
 - DRM_USAGEPOLICY_TYPE
---

# DRM_USAGEPOLICY_TYPE enumeration


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRM_USAGEPOLICY_TYPE</b> enumeration is used with the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetusagepolicy">DRMGetUsagePolicy</a> and <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetusagepolicy">DRMSetUsagePolicy</a> functions to specify a type of usage policy.

## -enum-fields

### -field DRM_USAGEPOLICY_TYPE_BYNAME

The usage policy is tied to an application name.

### -field DRM_USAGEPOLICY_TYPE_BYPUBLICKEY

The usage policy is tied to an application's public key.

### -field DRM_USAGEPOLICY_TYPE_BYDIGEST

The usage policy is tied to a digest of an application.

### -field DRM_USAGEPOLICY_TYPE_OSEXCLUSION

The usage policy is tied to an operating system.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetusagepolicy">DRMGetUsagePolicy</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetusagepolicy">DRMSetUsagePolicy</a>