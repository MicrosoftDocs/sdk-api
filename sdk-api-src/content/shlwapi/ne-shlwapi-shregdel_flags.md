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

# SHREGDEL_FLAGS enumeration


## -description


Provides a set of values that indicate from which base key an item will be deleted.


## -enum-fields




### -field SHREGDEL_DEFAULT

Deletes from <b>HKEY_CURRENT_USER</b>. If the specified item is not found under <b>HKEY_CURRENT_USER</b>, deletes from <b>HKEY_LOCAL_MACHINE</b>.


### -field SHREGDEL_HKCU

Enumerates from <b>HKEY_CURRENT_USER</b> only.


### -field SHREGDEL_HKLM

Enumerates under <b>HKEY_LOCAL_MACHINE</b> only.


### -field SHREGDEL_BOTH

Deletes from both <b>HKEY_CURRENT_USER</b> and <b>HKEY_LOCAL_MACHINE</b>.

