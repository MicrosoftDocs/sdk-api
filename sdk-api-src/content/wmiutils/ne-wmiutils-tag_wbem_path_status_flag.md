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

# tag_WBEM_PATH_STATUS_FLAG enumeration


## -description


Contains flags used to describe a path.


## -enum-fields




### -field WBEMPATH_INFO_ANON_LOCAL_MACHINE

Path has "." or <b>NULL</b> as the server name.


### -field WBEMPATH_INFO_HAS_MACHINE_NAME

Server name is specified in the path and that name is not ".".


### -field WBEMPATH_INFO_IS_CLASS_REF

There is a class part to the path, but it is not an instance.


### -field WBEMPATH_INFO_IS_INST_REF

There is a class part to the path and there are key values.


### -field WBEMPATH_INFO_HAS_SUBSCOPES

A subscope is present in the path. Currently WMI does not support scopes.


### -field WBEMPATH_INFO_IS_COMPOUND

Compound key is used.


### -field WBEMPATH_INFO_HAS_V2_REF_PATHS

One or more keys has a CIM reference.


### -field WBEMPATH_INFO_HAS_IMPLIED_KEY

Key names are missing somewhere in the path.


### -field WBEMPATH_INFO_CONTAINS_SINGLETON

One or more singletons.


### -field WBEMPATH_INFO_V1_COMPLIANT

No scopes and no CIM_REFERENCE keys.


### -field WBEMPATH_INFO_V2_COMPLIANT

Reserved. Do not use.


### -field WBEMPATH_INFO_CIM_COMPLIANT

Reserved. Do not use.


### -field WBEMPATH_INFO_IS_SINGLETON

Object is a singleton.


### -field WBEMPATH_INFO_IS_PARENT

Path is just "..".


### -field WBEMPATH_INFO_SERVER_NAMESPACE_ONLY

There is no class portion of the path.


### -field WBEMPATH_INFO_NATIVE_PATH

Path parser was initialized using 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a>.


### -field WBEMPATH_INFO_WMI_PATH

Reserved. Do not use.


### -field WBEMPATH_INFO_PATH_HAD_SERVER

Server name was set by either 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a> or 
<a href="https://msdn.microsoft.com/4da66edf-bf38-4246-82fc-27fd14e7d183">SetServer</a>.

