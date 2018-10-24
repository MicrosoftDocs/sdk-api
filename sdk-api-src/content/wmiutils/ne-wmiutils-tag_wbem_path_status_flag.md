---
UID: NE:wmiutils.tag_WBEM_PATH_STATUS_FLAG
title: tag_WBEM_PATH_STATUS_FLAG
author: windows-sdk-content
description: Contains flags used to describe a path.
old-location: wmi\tag_wbem_path_status_flag.htm
tech.root: WmiSdk
ms.assetid: 5dcc4432-e441-4e5a-b3f6-d90762b0d8f5
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WBEMPATH_INFO_ANON_LOCAL_MACHINE, WBEMPATH_INFO_CIM_COMPLIANT, WBEMPATH_INFO_CONTAINS_SINGLETON, WBEMPATH_INFO_HAS_IMPLIED_KEY, WBEMPATH_INFO_HAS_MACHINE_NAME, WBEMPATH_INFO_HAS_SUBSCOPES, WBEMPATH_INFO_HAS_V2_REF_PATHS, WBEMPATH_INFO_IS_CLASS_REF, WBEMPATH_INFO_IS_COMPOUND, WBEMPATH_INFO_IS_INST_REF, WBEMPATH_INFO_IS_PARENT, WBEMPATH_INFO_IS_SINGLETON, WBEMPATH_INFO_NATIVE_PATH, WBEMPATH_INFO_PATH_HAD_SERVER, WBEMPATH_INFO_SERVER_NAMESPACE_ONLY, WBEMPATH_INFO_V1_COMPLIANT, WBEMPATH_INFO_V2_COMPLIANT, WBEMPATH_INFO_WMI_PATH, tag_WBEM_PATH_STATUS_FLAG, tag_WBEM_PATH_STATUS_FLAG enumeration [Windows Management Instrumentation], wmi.tag_wbem_path_status_flag, wmiutils/WBEMPATH_INFO_ANON_LOCAL_MACHINE, wmiutils/WBEMPATH_INFO_CIM_COMPLIANT, wmiutils/WBEMPATH_INFO_CONTAINS_SINGLETON, wmiutils/WBEMPATH_INFO_HAS_IMPLIED_KEY, wmiutils/WBEMPATH_INFO_HAS_MACHINE_NAME, wmiutils/WBEMPATH_INFO_HAS_SUBSCOPES, wmiutils/WBEMPATH_INFO_HAS_V2_REF_PATHS, wmiutils/WBEMPATH_INFO_IS_CLASS_REF, wmiutils/WBEMPATH_INFO_IS_COMPOUND, wmiutils/WBEMPATH_INFO_IS_INST_REF, wmiutils/WBEMPATH_INFO_IS_PARENT, wmiutils/WBEMPATH_INFO_IS_SINGLETON, wmiutils/WBEMPATH_INFO_NATIVE_PATH, wmiutils/WBEMPATH_INFO_PATH_HAD_SERVER, wmiutils/WBEMPATH_INFO_SERVER_NAMESPACE_ONLY, wmiutils/WBEMPATH_INFO_V1_COMPLIANT, wmiutils/WBEMPATH_INFO_V2_COMPLIANT, wmiutils/WBEMPATH_INFO_WMI_PATH, wmiutils/tag_WBEM_PATH_STATUS_FLAG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WMIUtils.h
api_name:
 - tag_WBEM_PATH_STATUS_FLAG
product: Windows
targetos: Windows
req.typenames: tag_WBEM_PATH_STATUS_FLAG
req.redist: 
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

