---
UID: NS:wcmapi._WCM_PROFILE_INFO
title: WCM_PROFILE_INFO (wcmapi.h)
description: Contains information about a specific profile.
helpviewer_keywords: ["*PWCM_PROFILE_INFO","PWCM_PROFILE_INFO","PWCM_PROFILE_INFO structure pointer [Windows Connection Manager]","WCM_PROFILE_INFO","WCM_PROFILE_INFO structure [Windows Connection Manager]","wcm.wcm_profile_info","wcmapi/PWCM_PROFILE_INFO","wcmapi/WCM_PROFILE_INFO"]
old-location: wcm\wcm_profile_info.htm
tech.root: wcm
ms.assetid: bf917afa-c6c5-408a-bd34-b4a4c7b991b9
ms.date: 12/05/2018
ms.keywords: '*PWCM_PROFILE_INFO, PWCM_PROFILE_INFO, PWCM_PROFILE_INFO structure pointer [Windows Connection Manager], WCM_PROFILE_INFO, WCM_PROFILE_INFO structure [Windows Connection Manager], wcm.wcm_profile_info, wcmapi/PWCM_PROFILE_INFO, wcmapi/WCM_PROFILE_INFO'
req.header: wcmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WCM_PROFILE_INFO, *PWCM_PROFILE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WCM_PROFILE_INFO
 - wcmapi/_WCM_PROFILE_INFO
 - PWCM_PROFILE_INFO
 - wcmapi/PWCM_PROFILE_INFO
 - WCM_PROFILE_INFO
 - wcmapi/WCM_PROFILE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_PROFILE_INFO
---

# WCM_PROFILE_INFO structure


## -description

The <b>WCM_PROFILE_INFO</b> structure contains information about a specific profile.

## -struct-fields

### -field strProfileName

Type: <b>WCHAR[WCM_MAX_PROFILE_NAME]</b>

The profile name.

### -field AdapterGUID

Type: <b>GUID</b>

The GUID of the adapter.

### -field Media

Type: <b><a href="/windows/desktop/api/wcmapi/ne-wcmapi-wcm_media_type">WCM_MEDIA_TYPE</a></b>

The media type for the profile.

## -see-also

<a href="/windows/desktop/api/wcmapi/ne-wcmapi-wcm_media_type">WCM_MEDIA_TYPE</a>