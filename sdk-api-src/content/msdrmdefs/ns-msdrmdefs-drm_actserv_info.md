---
UID: NS:msdrmdefs._DRM_ACTSERV_INFO
title: DRM_ACTSERV_INFO (msdrmdefs.h)
description: The DRM_ACTSERV_INFO structure stores information about the activation server.
helpviewer_keywords: ["DRM_ACTSERV_INFO","DRM_ACTSERV_INFO structure [Active Directory Rights Management Services SDK 1.0]","msdrmdefs/DRM_ACTSERV_INFO","rm.drm_actserv_info"]
old-location: rm\drm_actserv_info.htm
tech.root: rm
ms.assetid: 2ea83a08-ab86-4635-8684-519808430ce9
ms.date: 12/05/2018
ms.keywords: DRM_ACTSERV_INFO, DRM_ACTSERV_INFO structure [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRM_ACTSERV_INFO, rm.drm_actserv_info
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
req.typenames: DRM_ACTSERV_INFO
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRM_ACTSERV_INFO
 - msdrmdefs/_DRM_ACTSERV_INFO
 - DRM_ACTSERV_INFO
 - msdrmdefs/DRM_ACTSERV_INFO
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
 - DRM_ACTSERV_INFO
---

# DRM_ACTSERV_INFO structure


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRM_ACTSERV_INFO</b> structure stores information about the activation server.

## -struct-fields

### -field uVersion

Version of this structure, for backward compatibility. When using C, this value should be initialized to <b>DRMACTSERVINFOVERSION</b>. In C++ this is done automatically.

### -field wszPubKey

This member is reserved and must be set to <b>NULL</b>.

### -field wszURL

URL for a service that performs activation. Use <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetservicelocation">DRMGetServiceLocation</a> to find a service location if none is known, or pass in <b>NULL</b> to use Passport service discovery. The URL should have the form <b>http://</b><i>CompanyName</i><b>/_wmcs/certification</b>, for example, http://blueyonderairlines/_wmcs/certification. The parameter defaults to <b>NULL</b> in C++.

### -field _DRM_ACTSERV_INFO

TBD

## -remarks

This structure has a C++ default constructor that takes no parameters and sets members to the default values described above.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-structures">AD RMS Structures</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmisactivated">DRMIsActivated</a>