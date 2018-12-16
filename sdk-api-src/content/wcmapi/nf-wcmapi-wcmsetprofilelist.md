---
UID: NF:wcmapi.WcmSetProfileList
title: WcmSetProfileList function
author: windows-sdk-content
description: Reorders a profile list or a subset of a profile list.
old-location: wcm\wcmsetprofilelist.htm
tech.root: wcm
ms.assetid: c5efb2e8-c4c4-4e13-9f7a-ea2a40744655
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WcmSetProfileList, WcmSetProfileList function [Windows Connection Manager], wcm.wcmsetprofilelist, wcmapi/WcmSetProfileList
ms.topic: function
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
 - Ext-MS-Win-networking-wcmapi-l1-1-0.dll
api_name:
 - WcmSetProfileList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcmSetProfileList function


## -description


The <b>WcmSetProfileList</b> function reorders a profile list or a subset of a profile list.


## -parameters




### -param pProfileList [in]

Type: <b><a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">WCM_PROFILE_INFO_LIST</a>*</b>

The list of profiles to be reordered, provided in the preferred order (descending from the most preferred to the least preferred).


### -param dwPosition [in]

Type: <b>DWORD</b>

Specifies the position in the list to start the reorder.


### -param fIgnoreUnknownProfiles [in]

Type: <b>BOOL</b>

True if any profiles in <i>pProfileList</i> which do not exist should be ignored; the call will proceed with the remainder of the list. False if the call should fail without modifying the profile order if any profiles in <i>pProfileList</i> do not exist.


### -param pReserved

Type: <b>PVOID</b>

Reserved.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">WCM_PROFILE_INFO_LIST</a>
 

 

