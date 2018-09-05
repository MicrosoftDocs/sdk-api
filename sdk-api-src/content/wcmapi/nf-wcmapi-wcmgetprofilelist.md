---
UID: NF:wcmapi.WcmGetProfileList
title: WcmGetProfileList function
author: windows-sdk-content
description: Retrieves a list of profiles in preferred order.
old-location: wcm\wcmgetprofilelist.htm
old-project: wcm
ms.assetid: ceef4e74-3c67-4267-a82a-9912c039f41c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WcmGetProfileList, WcmGetProfileList function [Windows Connection Manager], wcm.wcmgetprofilelist, wcmapi/WcmGetProfileList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WCM_PROPERTY, *PWCM_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wcmapi.dll
api_name:
 - WcmGetProfileList
product: Windows
targetos: Windows
req.lib: Wcmapi.lib
req.dll: Wcmapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WcmGetProfileList function


## -description


The <b>WcmGetProfileList</b> function retrieves a list of profiles in preferred order, descending from the most preferred to the least preferred. The list includes all WCM-managed auto-connect profiles across all WCM-managed media types.


## -parameters




### -param pReserved

Type: <b>PVOID</b>

Reserved.


### -param ppProfileList [out]

Type: <b><a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">PWCM_PROFILE_INFO_LIST</a>*</b>

The list of profiles.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">PWCM_PROFILE_INFO_LIST</a>
 

 

