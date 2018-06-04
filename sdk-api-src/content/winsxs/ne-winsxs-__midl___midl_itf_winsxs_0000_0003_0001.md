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

# __MIDL___MIDL_itf_winsxs_0000_0003_0001 enumeration


## -description


The <b>CREATE_ASM_NAME_OBJ_FLAGS</b> enumeration is used by the <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> function.

If no  value is specified, the <i>szAssemblyName</i> parameter of the <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> function is the "Name" portion of the fully-specified assembly name.


## -enum-fields




### -field CANOF_PARSE_DISPLAY_NAME

If this flag is specified, the <i>szAssemblyName</i> parameter of <a href="https://msdn.microsoft.com/1290a0b3-28f9-46fb-a98f-40b43bc0df1a">CreateAssemblyNameObject</a> is a fully-specified side-by-side assembly name and is parsed to the individual properties.


### -field CANOF_SET_DEFAULT_VALUES

Reserved.

