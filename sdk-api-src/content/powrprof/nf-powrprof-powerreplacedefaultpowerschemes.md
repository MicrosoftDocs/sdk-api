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

# PowerReplaceDefaultPowerSchemes function


## -description


Replaces the default power schemes with the current user's power schemes. This allows an 
    administrator to change the default power schemes for the system. Replacing the default schemes enables users to 
    use the <b>Restore Defaults</b> option in the Control Panel 
    <b>Power Options</b> application to restore customized power scheme defaults instead of the 
    original Windows power scheme defaults.


## -parameters






## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -remarks



The caller must be a member of the local Administrators group.



