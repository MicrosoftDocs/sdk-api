---
UID: NS:wcmapi._WCM_PROFILE_INFO_LIST
title: WCM_PROFILE_INFO_LIST (wcmapi.h)
description: Contains a list of profiles in preferred order.
helpviewer_keywords: ["*PWCM_PROFILE_INFO_LIST","PWCM_PROFILE_INFO_LIST","PWCM_PROFILE_INFO_LIST structure pointer [Windows Connection Manager]","WCM_PROFILE_INFO_LIST","WCM_PROFILE_INFO_LIST structure [Windows Connection Manager]","wcm.wcm_profile_info_list","wcmapi/PWCM_PROFILE_INFO_LIST","wcmapi/WCM_PROFILE_INFO_LIST"]
old-location: wcm\wcm_profile_info_list.htm
tech.root: wcm
ms.assetid: 73ddb610-233a-470b-900d-ae62a1e7121a
ms.date: 12/05/2018
ms.keywords: '*PWCM_PROFILE_INFO_LIST, PWCM_PROFILE_INFO_LIST, PWCM_PROFILE_INFO_LIST structure pointer [Windows Connection Manager], WCM_PROFILE_INFO_LIST, WCM_PROFILE_INFO_LIST structure [Windows Connection Manager], wcm.wcm_profile_info_list, wcmapi/PWCM_PROFILE_INFO_LIST, wcmapi/WCM_PROFILE_INFO_LIST'
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
req.typenames: WCM_PROFILE_INFO_LIST, *PWCM_PROFILE_INFO_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WCM_PROFILE_INFO_LIST
 - wcmapi/_WCM_PROFILE_INFO_LIST
 - PWCM_PROFILE_INFO_LIST
 - wcmapi/PWCM_PROFILE_INFO_LIST
 - WCM_PROFILE_INFO_LIST
 - wcmapi/WCM_PROFILE_INFO_LIST
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
 - WCM_PROFILE_INFO_LIST
---

# WCM_PROFILE_INFO_LIST structure


## -description

The <b>WCM_PROFILE_INFO_LIST</b> structure contains a list of profiles in preferred order.

## -struct-fields

### -field dwNumberOfItems

Type: <b>DWORD</b>

The number of profiles in the list.

### -field ProfileInfo.unique

### -field ProfileInfo.size_is

### -field ProfileInfo.size_is.dwNumberOfItems

### -field ProfileInfo

Type: <b><a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_profile_info">WCM_PROFILE_INFO</a>[1]</b>

Information about each profile.

## -see-also

<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_profile_info">WCM_PROFILE_INFO</a>