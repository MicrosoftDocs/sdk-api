---
UID: NS:wcmapi._WCM_PROFILE_INFO_LIST
title: "_WCM_PROFILE_INFO_LIST"
author: windows-sdk-content
description: Contains a list of profiles in preferred order.
old-location: wcm\wcm_profile_info_list.htm
tech.root: wcm
ms.assetid: 73ddb610-233a-470b-900d-ae62a1e7121a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PWCM_PROFILE_INFO_LIST, PWCM_PROFILE_INFO_LIST, PWCM_PROFILE_INFO_LIST structure pointer [Windows Connection Manager], WCM_PROFILE_INFO_LIST, WCM_PROFILE_INFO_LIST structure [Windows Connection Manager], _WCM_PROFILE_INFO_LIST, wcm.wcm_profile_info_list, wcmapi/PWCM_PROFILE_INFO_LIST, wcmapi/WCM_PROFILE_INFO_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# _WCM_PROFILE_INFO_LIST structure


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

Type: <b><a href="https://msdn.microsoft.com/bf917afa-c6c5-408a-bd34-b4a4c7b991b9">WCM_PROFILE_INFO</a>[1]</b>

Information about each profile.


## -see-also




<a href="https://msdn.microsoft.com/bf917afa-c6c5-408a-bd34-b4a4c7b991b9">WCM_PROFILE_INFO</a>
 

 

