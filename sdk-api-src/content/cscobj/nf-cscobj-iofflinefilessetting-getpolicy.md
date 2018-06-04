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

# IOfflineFilesSetting::GetPolicy


## -description


Retrieves a policy associated with a particular Offline Files setting.


## -parameters




### -param pvarValue [out]

If the policy supports one or more values, the returned <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> object contains those values.  If the policy does not support values, the type of the returned <b>VARIANT</b> is <b>VT_EMPTY</b>.

The method initializes the <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> prior to storing the policy value in it.


### -param dwScope [in]

Indicates which policy is to be retrieved.  Must be one of the following.

<div class="alert"><b>Note</b>  Note that not all settings have an associated policy and those that do might not support both per-machine and per-user policy.</div>
<div> </div>


#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The per-user policy is to be retrieved.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The per-machine policy is to be retrieved.


## -returns



<b>S_OK</b> if the policy is read successfully or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</code> if the setting does not support the requested policy.

Returns <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the requested policy is not currently applied.




## -remarks



It is important to note that policy cannot be set through the Offline Files API.  Policy can be set only through the Group Policy mechanism.  The Offline Files API only supports querying policy values.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

