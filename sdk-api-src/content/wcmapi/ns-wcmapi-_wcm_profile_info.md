---
UID: NS:wcmapi._WCM_PROFILE_INFO
title: "_WCM_PROFILE_INFO"
author: windows-sdk-content
description: Contains information about a specific profile.
old-location: wcm\wcm_profile_info.htm
old-project: wcm
ms.assetid: bf917afa-c6c5-408a-bd34-b4a4c7b991b9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWCM_PROFILE_INFO, PWCM_PROFILE_INFO, PWCM_PROFILE_INFO structure pointer [Windows Connection Manager], WCM_PROFILE_INFO, WCM_PROFILE_INFO structure [Windows Connection Manager], _WCM_PROFILE_INFO, wcm.wcm_profile_info, wcmapi/PWCM_PROFILE_INFO, wcmapi/WCM_PROFILE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wcmapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WCM_PROFILE_INFO, *PWCM_PROFILE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_PROFILE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WCM_PROFILE_INFO structure


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

Type: <b><a href="https://msdn.microsoft.com/76617f35-c7a1-49ff-a630-482f2fe45dd7">WCM_MEDIA_TYPE</a></b>

The media type for the profile.


## -see-also




<a href="https://msdn.microsoft.com/76617f35-c7a1-49ff-a630-482f2fe45dd7">WCM_MEDIA_TYPE</a>
 

 

