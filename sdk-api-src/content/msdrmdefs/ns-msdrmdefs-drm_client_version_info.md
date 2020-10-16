---
UID: NS:msdrmdefs._DRM_CLIENT_VERSION_INFO
title: DRM_CLIENT_VERSION_INFO (msdrmdefs.h)
description: Receives information about the version of the Active Directory Rights Management Services (AD RMS) client and the hierarchy, such as Production or Pre-production.
helpviewer_keywords: ["DRM_CLIENT_VERSION_INFO","DRM_CLIENT_VERSION_INFO structure [Active Directory Rights Management Services SDK 1.0]","dwVersion","msdrmdefs/DRM_CLIENT_VERSION_INFO","rm.drm_client_version_info"]
old-location: rm\drm_client_version_info.htm
tech.root: rm
ms.assetid: 5f1fdd8a-dbe1-4b07-888b-b5af0f593fd3
ms.date: 12/05/2018
ms.keywords: DRM_CLIENT_VERSION_INFO, DRM_CLIENT_VERSION_INFO structure [Active Directory Rights Management Services SDK 1.0], dwVersion, msdrmdefs/DRM_CLIENT_VERSION_INFO, rm.drm_client_version_info
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
req.typenames: DRM_CLIENT_VERSION_INFO
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRM_CLIENT_VERSION_INFO
 - msdrmdefs/_DRM_CLIENT_VERSION_INFO
 - DRM_CLIENT_VERSION_INFO
 - msdrmdefs/DRM_CLIENT_VERSION_INFO
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
 - DRM_CLIENT_VERSION_INFO
---

# DRM_CLIENT_VERSION_INFO structure


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRM_CLIENT_VERSION_INFO</b> structure receives information about the version of the Active Directory Rights Management Services (AD RMS) client and the hierarchy, such as Production or Pre-production. This structure is used by the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetclientversion">DRMGetClientVersion</a> function.

## -struct-fields

### -field uStructVersion

Version of this structure, for backward compatibility. In C, this value should be initialized to <b>DRMCLIENTSTRUCTVERSION</b>.

### -field dwVersion

Array of type <b>DWORD</b> that receives the version number of the Active Directory Rights Management Services client software. The version number consists of the following parts.



#### dwVersion (0)

The client major version number.



#### dwVersion (1)

The client minor version number.



#### dwVersion (2)

The client build version number.



#### dwVersion (3)

The client private version number.

### -field wszHierarchy

Array of type <b>WCHAR</b> that receives the hierarchy information, such as Production or Pre-production.

### -field wszProductId

Array of type <b>WCHAR</b> that receives the product ID. This member  is not currently filled by the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetclientversion">DRMGetClientVersion</a> function.

### -field wszProductDescription

Array of type <b>WCHAR</b> that receives the product description. This member is not currently filled by the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetclientversion">DRMGetClientVersion</a> function.

### -field _DRM_CLIENT_VERSION_INFO

TBD


## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-structures">AD RMS Structures</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetclientversion">DRMGetClientVersion</a>