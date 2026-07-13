---
UID: NF:wcmapi.WcmGetProfileList
title: WcmGetProfileList function (wcmapi.h)
description: Retrieves a list of profiles in preferred order.
helpviewer_keywords: ["WcmGetProfileList","WcmGetProfileList function [Windows Connection Manager]","wcm.wcmgetprofilelist","wcmapi/WcmGetProfileList"]
old-location: wcm\wcmgetprofilelist.htm
tech.root: wcm
ms.assetid: ceef4e74-3c67-4267-a82a-9912c039f41c
ms.date: 12/05/2018
ms.keywords: WcmGetProfileList, WcmGetProfileList function [Windows Connection Manager], wcm.wcmgetprofilelist, wcmapi/WcmGetProfileList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WcmGetProfileList
 - wcmapi/WcmGetProfileList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-networking-wcmapi-l1-1-1.dll
 - ext-ms-win-networking-wcmapi-l1-1-0.dll
 - Wcmapi.dll
api_name:
 - WcmGetProfileList
---

# WcmGetProfileList function


## -description

The <b>WcmGetProfileList</b> function retrieves a list of profiles in preferred order, descending from the most preferred to the least preferred. The list includes all WCM-managed auto-connect profiles across all WCM-managed media types.

## -parameters

### -param pReserved

Type: <b>PVOID</b>

Reserved.

### -param ppProfileList [out]

Type: <b><a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_profile_info_list">PWCM_PROFILE_INFO_LIST</a>*</b>

The list of profiles.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_profile_info_list">PWCM_PROFILE_INFO_LIST</a>