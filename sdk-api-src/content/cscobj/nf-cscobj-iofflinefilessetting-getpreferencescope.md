---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IOfflineFilesSetting::GetPreferenceScope


## -description



    Indicates the scope of the preference associated with this setting.


## -parameters




### -param pdwScope [out]

Receives the supported scope of the policy for this setting.  This scope can be one or both of the following values.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The setting supports per-user preference.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The setting supports per-machine preference.


## -returns



S_OK if the scope is returned successfully or an error value otherwise.




## -remarks



Note that this is an indication of the supported scopes, not of the applied scopes.  For example, a setting may recognize both per-user and per-machine preference yet only the per-user preference has been applied.  In this scenario, this method would return both OFFLINEFILES_SETTING_SCOPE_USER and OFFLINEFILES_SETTING_SCOPE_COMPUTER.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

