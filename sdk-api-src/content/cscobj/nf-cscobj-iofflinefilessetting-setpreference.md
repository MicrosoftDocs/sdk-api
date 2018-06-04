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

# IOfflineFilesSetting::SetPreference


## -description


Sets a per-computer or per-user preference associated with an Offline Files setting.


## -parameters




### -param pvarValue [in]

Specifies the value associated with the preference.

If multiple values are associated with the preference, the <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> type includes <b>VT_ARRAY</b> and the values are stored in a <b>SAFEARRAY</b>.


### -param dwScope [in]

Indicates if the preference to be set is per-user or per-machine.  Must be one of the following.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The per-user preference is to be set.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The per-machine preference is to be set.


## -returns



<b>S_OK</b> if the preference is set successfully or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)</code> if one or more data values specified via <i>pvtValue</i> are not valid.

Returns <code>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</code> if the caller is trying to set a per-machine preference and is not a local administrator.

Returns <code>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</code> if a scope is specified that is not supported by the preference.




## -remarks



This method requires system administrator privileges if the preference is a per-machine preference.

It is important to note that policy cannot be set through the Offline Files API.  Policy can be set only through the Group Policy mechanism.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

