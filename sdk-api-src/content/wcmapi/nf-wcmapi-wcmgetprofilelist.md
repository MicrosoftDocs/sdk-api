---
UID: NF:wcmapi.WcmGetProfileList
title: WcmGetProfileList function (wcmapi.h)
author: windows-sdk-content
description: Retrieves a list of profiles in preferred order.
old-location: wcm\wcmgetprofilelist.htm
tech.root: wcm
ms.assetid: ceef4e74-3c67-4267-a82a-9912c039f41c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WcmGetProfileList, WcmGetProfileList function [Windows Connection Manager], wcm.wcmgetprofilelist, wcmapi/WcmGetProfileList
ms.topic: function
f1_keywords:
- wcmapi/WcmGetProfileList
dev_langs:
 - c++
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
req.lib: Wcmapi.lib
req.dll: Wcmapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wcmapi.dll
api_name:
- WcmGetProfileList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WcmGetProfileList function


## -description


The <b>WcmGetProfileList</b> function retrieves a list of profiles in preferred order, descending from the most preferred to the least preferred. The list includes all WCM-managed auto-connect profiles across all WCM-managed media types.


## -parameters




### -param pReserved

Type: <b>PVOID</b>

Reserved.


### -param ppProfileList [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wcmapi/ns-wcmapi-wcm_profile_info_list">PWCM_PROFILE_INFO_LIST</a>*</b>

The list of profiles.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wcmapi/ns-wcmapi-wcm_profile_info_list">PWCM_PROFILE_INFO_LIST</a>
 

 

