---
UID: NS:wcmapi._WCM_PROFILE_INFO_LIST
title: WCM_PROFILE_INFO_LIST (wcmapi.h)
author: windows-sdk-content
description: Contains a list of profiles in preferred order.
old-location: wcm\wcm_profile_info_list.htm
tech.root: wcm
ms.assetid: 73ddb610-233a-470b-900d-ae62a1e7121a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWCM_PROFILE_INFO_LIST, PWCM_PROFILE_INFO_LIST, PWCM_PROFILE_INFO_LIST structure pointer [Windows Connection Manager], WCM_PROFILE_INFO_LIST, WCM_PROFILE_INFO_LIST structure [Windows Connection Manager], wcm.wcm_profile_info_list, wcmapi/PWCM_PROFILE_INFO_LIST, wcmapi/WCM_PROFILE_INFO_LIST"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_PROFILE_INFO_LIST
product: Windows
targetos: Windows
req.typenames: WCM_PROFILE_INFO_LIST, *PWCM_PROFILE_INFO_LIST
req.redist: 
ms.custom: 19H1
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

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wcmapi/ns-wcmapi-_wcm_profile_info">WCM_PROFILE_INFO</a>[1]</b>

Information about each profile.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wcmapi/ns-wcmapi-_wcm_profile_info">WCM_PROFILE_INFO</a>
 

 

