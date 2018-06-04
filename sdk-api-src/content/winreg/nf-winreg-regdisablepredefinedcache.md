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

# RegDisablePredefinedCache function


## -description


Disables handle caching of the predefined registry handle for <b>HKEY_CURRENT_USER</b> for the current process. This function does not work on a remote computer.

To disables handle caching of all predefined registry handles, use the <a href="https://msdn.microsoft.com/a56cf7d9-0ac4-4719-af41-3c0cdcef6faf">RegDisablePredefinedCacheEx</a> function.


## -parameters






## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Any access of <b>HKEY_CURRENT_USER</b> after this function is called will result in operations being performed on <b>HKEY_USERS</b>\<b>SID_of_current_user</b>,  or on <b>HKEY_USERS\.DEFAULT</b> if the current user's hive is not loaded. For more information on SIDs, see 
<a href="security.security_identifiers_sids_">Security Identifiers</a>.




## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">Predefined Keys</a>



<a href="https://msdn.microsoft.com/a56cf7d9-0ac4-4719-af41-3c0cdcef6faf">RegDisablePredefinedCacheEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

