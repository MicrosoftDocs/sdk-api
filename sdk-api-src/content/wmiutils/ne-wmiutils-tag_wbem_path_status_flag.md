---
UID: NE:wmiutils.tag_WBEM_PATH_STATUS_FLAG
title: tag_WBEM_PATH_STATUS_FLAG (wmiutils.h)
description: Contains flags used to describe a path.
helpviewer_keywords: ["WBEMPATH_INFO_ANON_LOCAL_MACHINE","WBEMPATH_INFO_CIM_COMPLIANT","WBEMPATH_INFO_CONTAINS_SINGLETON","WBEMPATH_INFO_HAS_IMPLIED_KEY","WBEMPATH_INFO_HAS_MACHINE_NAME","WBEMPATH_INFO_HAS_SUBSCOPES","WBEMPATH_INFO_HAS_V2_REF_PATHS","WBEMPATH_INFO_IS_CLASS_REF","WBEMPATH_INFO_IS_COMPOUND","WBEMPATH_INFO_IS_INST_REF","WBEMPATH_INFO_IS_PARENT","WBEMPATH_INFO_IS_SINGLETON","WBEMPATH_INFO_NATIVE_PATH","WBEMPATH_INFO_PATH_HAD_SERVER","WBEMPATH_INFO_SERVER_NAMESPACE_ONLY","WBEMPATH_INFO_V1_COMPLIANT","WBEMPATH_INFO_V2_COMPLIANT","WBEMPATH_INFO_WMI_PATH","tag_WBEM_PATH_STATUS_FLAG","tag_WBEM_PATH_STATUS_FLAG enumeration [Windows Management Instrumentation]","wmi.tag_wbem_path_status_flag","wmiutils/WBEMPATH_INFO_ANON_LOCAL_MACHINE","wmiutils/WBEMPATH_INFO_CIM_COMPLIANT","wmiutils/WBEMPATH_INFO_CONTAINS_SINGLETON","wmiutils/WBEMPATH_INFO_HAS_IMPLIED_KEY","wmiutils/WBEMPATH_INFO_HAS_MACHINE_NAME","wmiutils/WBEMPATH_INFO_HAS_SUBSCOPES","wmiutils/WBEMPATH_INFO_HAS_V2_REF_PATHS","wmiutils/WBEMPATH_INFO_IS_CLASS_REF","wmiutils/WBEMPATH_INFO_IS_COMPOUND","wmiutils/WBEMPATH_INFO_IS_INST_REF","wmiutils/WBEMPATH_INFO_IS_PARENT","wmiutils/WBEMPATH_INFO_IS_SINGLETON","wmiutils/WBEMPATH_INFO_NATIVE_PATH","wmiutils/WBEMPATH_INFO_PATH_HAD_SERVER","wmiutils/WBEMPATH_INFO_SERVER_NAMESPACE_ONLY","wmiutils/WBEMPATH_INFO_V1_COMPLIANT","wmiutils/WBEMPATH_INFO_V2_COMPLIANT","wmiutils/WBEMPATH_INFO_WMI_PATH","wmiutils/tag_WBEM_PATH_STATUS_FLAG"]
old-location: wmi\tag_wbem_path_status_flag.htm
tech.root: wmi
ms.assetid: 5dcc4432-e441-4e5a-b3f6-d90762b0d8f5
ms.date: 12/05/2018
ms.keywords: WBEMPATH_INFO_ANON_LOCAL_MACHINE, WBEMPATH_INFO_CIM_COMPLIANT, WBEMPATH_INFO_CONTAINS_SINGLETON, WBEMPATH_INFO_HAS_IMPLIED_KEY, WBEMPATH_INFO_HAS_MACHINE_NAME, WBEMPATH_INFO_HAS_SUBSCOPES, WBEMPATH_INFO_HAS_V2_REF_PATHS, WBEMPATH_INFO_IS_CLASS_REF, WBEMPATH_INFO_IS_COMPOUND, WBEMPATH_INFO_IS_INST_REF, WBEMPATH_INFO_IS_PARENT, WBEMPATH_INFO_IS_SINGLETON, WBEMPATH_INFO_NATIVE_PATH, WBEMPATH_INFO_PATH_HAD_SERVER, WBEMPATH_INFO_SERVER_NAMESPACE_ONLY, WBEMPATH_INFO_V1_COMPLIANT, WBEMPATH_INFO_V2_COMPLIANT, WBEMPATH_INFO_WMI_PATH, tag_WBEM_PATH_STATUS_FLAG, tag_WBEM_PATH_STATUS_FLAG enumeration [Windows Management Instrumentation], wmi.tag_wbem_path_status_flag, wmiutils/WBEMPATH_INFO_ANON_LOCAL_MACHINE, wmiutils/WBEMPATH_INFO_CIM_COMPLIANT, wmiutils/WBEMPATH_INFO_CONTAINS_SINGLETON, wmiutils/WBEMPATH_INFO_HAS_IMPLIED_KEY, wmiutils/WBEMPATH_INFO_HAS_MACHINE_NAME, wmiutils/WBEMPATH_INFO_HAS_SUBSCOPES, wmiutils/WBEMPATH_INFO_HAS_V2_REF_PATHS, wmiutils/WBEMPATH_INFO_IS_CLASS_REF, wmiutils/WBEMPATH_INFO_IS_COMPOUND, wmiutils/WBEMPATH_INFO_IS_INST_REF, wmiutils/WBEMPATH_INFO_IS_PARENT, wmiutils/WBEMPATH_INFO_IS_SINGLETON, wmiutils/WBEMPATH_INFO_NATIVE_PATH, wmiutils/WBEMPATH_INFO_PATH_HAD_SERVER, wmiutils/WBEMPATH_INFO_SERVER_NAMESPACE_ONLY, wmiutils/WBEMPATH_INFO_V1_COMPLIANT, wmiutils/WBEMPATH_INFO_V2_COMPLIANT, wmiutils/WBEMPATH_INFO_WMI_PATH, wmiutils/tag_WBEM_PATH_STATUS_FLAG
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
targetos: Windows
req.typenames: tag_WBEM_PATH_STATUS_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_PATH_STATUS_FLAG
 - wmiutils/tag_WBEM_PATH_STATUS_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WMIUtils.h
api_name:
 - tag_WBEM_PATH_STATUS_FLAG
---

# tag_WBEM_PATH_STATUS_FLAG enumeration


## -description

Contains flags used to describe a path.

## -enum-fields

### -field WBEMPATH_INFO_ANON_LOCAL_MACHINE:0x1

Path has "." or <b>NULL</b> as the server name.

### -field WBEMPATH_INFO_HAS_MACHINE_NAME:0x2

Server name is specified in the path and that name is not ".".

### -field WBEMPATH_INFO_IS_CLASS_REF:0x4

There is a class part to the path, but it is not an instance.

### -field WBEMPATH_INFO_IS_INST_REF:0x8

There is a class part to the path and there are key values.

### -field WBEMPATH_INFO_HAS_SUBSCOPES:0x10

A subscope is present in the path. Currently WMI does not support scopes.

### -field WBEMPATH_INFO_IS_COMPOUND:0x20

Compound key is used.

### -field WBEMPATH_INFO_HAS_V2_REF_PATHS:0x40

One or more keys has a CIM reference.

### -field WBEMPATH_INFO_HAS_IMPLIED_KEY:0x80

Key names are missing somewhere in the path.

### -field WBEMPATH_INFO_CONTAINS_SINGLETON:0x100

One or more singletons.

### -field WBEMPATH_INFO_V1_COMPLIANT:0x200

No scopes and no CIM_REFERENCE keys.

### -field WBEMPATH_INFO_V2_COMPLIANT:0x400

Reserved. Do not use.

### -field WBEMPATH_INFO_CIM_COMPLIANT:0x800

Reserved. Do not use.

### -field WBEMPATH_INFO_IS_SINGLETON:0x1000

Object is a singleton.

### -field WBEMPATH_INFO_IS_PARENT:0x2000

Path is just "..".

### -field WBEMPATH_INFO_SERVER_NAMESPACE_ONLY:0x4000

There is no class portion of the path.

### -field WBEMPATH_INFO_NATIVE_PATH:0x8000

Path parser was initialized using 
<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-settext">SetText</a>.

### -field WBEMPATH_INFO_WMI_PATH:0x10000

Reserved. Do not use.

### -field WBEMPATH_INFO_PATH_HAD_SERVER:0x20000

Server name was set by either 
<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-settext">SetText</a> or 
<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-setserver">SetServer</a>.
