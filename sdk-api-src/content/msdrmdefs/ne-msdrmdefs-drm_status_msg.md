---
UID: NE:msdrmdefs._DRM_STATUS_MSG
title: DRM_STATUS_MSG (msdrmdefs.h)
description: Used by the custom callback function to specify why the callback function is being called.
helpviewer_keywords: ["DRM_MSG_ACQUIRE_ADVISORY","DRM_MSG_ACQUIRE_CLIENTLICENSOR","DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE","DRM_MSG_ACQUIRE_LICENSE","DRM_MSG_ACTIVATE_GROUPIDENTITY","DRM_MSG_ACTIVATE_MACHINE","DRM_MSG_SIGN_ISSUANCE_LICENSE","DRM_STATUS_MSG","DRM_STATUS_MSG enumeration [Active Directory Rights Management Services SDK 1.0]","msdrmdefs/DRM_MSG_ACQUIRE_ADVISORY","msdrmdefs/DRM_MSG_ACQUIRE_CLIENTLICENSOR","msdrmdefs/DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE","msdrmdefs/DRM_MSG_ACQUIRE_LICENSE","msdrmdefs/DRM_MSG_ACTIVATE_GROUPIDENTITY","msdrmdefs/DRM_MSG_ACTIVATE_MACHINE","msdrmdefs/DRM_MSG_SIGN_ISSUANCE_LICENSE","msdrmdefs/DRM_STATUS_MSG","rm.drm_status_msg"]
old-location: rm\drm_status_msg.htm
tech.root: rm
ms.assetid: 9420c415-09ef-43a0-b458-bfaae9857314
ms.date: 12/05/2018
ms.keywords: DRM_MSG_ACQUIRE_ADVISORY, DRM_MSG_ACQUIRE_CLIENTLICENSOR, DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE, DRM_MSG_ACQUIRE_LICENSE, DRM_MSG_ACTIVATE_GROUPIDENTITY, DRM_MSG_ACTIVATE_MACHINE, DRM_MSG_SIGN_ISSUANCE_LICENSE, DRM_STATUS_MSG, DRM_STATUS_MSG enumeration [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRM_MSG_ACQUIRE_ADVISORY, msdrmdefs/DRM_MSG_ACQUIRE_CLIENTLICENSOR, msdrmdefs/DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE, msdrmdefs/DRM_MSG_ACQUIRE_LICENSE, msdrmdefs/DRM_MSG_ACTIVATE_GROUPIDENTITY, msdrmdefs/DRM_MSG_ACTIVATE_MACHINE, msdrmdefs/DRM_MSG_SIGN_ISSUANCE_LICENSE, msdrmdefs/DRM_STATUS_MSG, rm.drm_status_msg
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
req.typenames: DRM_STATUS_MSG
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRM_STATUS_MSG
 - msdrmdefs/_DRM_STATUS_MSG
 - DRM_STATUS_MSG
 - msdrmdefs/DRM_STATUS_MSG
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
 - DRM_STATUS_MSG
---

# DRM_STATUS_MSG enumeration


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRM_STATUS_MSG</b> enumeration is used by the custom callback function to specify why the callback function is being called.

## -enum-fields

### -field DRM_MSG_ACTIVATE_MACHINE

AD RMS is attempting to activate the machine. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-activate-machine">DRM_MSG_ACTIVATE_MACHINE</a> message.

### -field DRM_MSG_ACTIVATE_GROUPIDENTITY

AD RMS is attempting to activate a user. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-activate-groupidentity">DRM_MSG_ACTIVATE_GROUPIDENTITY</a> message.

### -field DRM_MSG_ACQUIRE_LICENSE

AD RMS is attempting to acquire a license. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-license">DRM_MSG_ACQUIRE_LICENSE</a> message.

### -field DRM_MSG_ACQUIRE_ADVISORY

AD RMS is attempting to acquire a revocation list. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-advisory">DRM_MSG_ACQUIRE_ADVISORY</a> message.

### -field DRM_MSG_SIGN_ISSUANCE_LICENSE

AD RMS is attempting to acquire a signed issuance license. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-sign-issuance-license">DRM_MSG_SIGN_ISSUANCE_LICENSE</a> message.

### -field DRM_MSG_ACQUIRE_CLIENTLICENSOR

AD RMS is attempting to acquire a client licensor certificate. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-clientlicensor">DRM_MSG_ACQUIRE_CLIENTLICENSOR</a> message.

### -field DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE

AD RMS is attempting to acquire a template collection. For more information, see the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-issuance-license-template">DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE</a> message.

## -remarks

The callback function can use this message, together with the <i>hr</i> parameter, to determine the status of a request to a server.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquireadvisories">DRMAcquireAdvisories</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>