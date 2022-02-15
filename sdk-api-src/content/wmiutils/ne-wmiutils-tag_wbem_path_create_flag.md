---
UID: NE:wmiutils.tag_WBEM_PATH_CREATE_FLAG
title: tag_WBEM_PATH_CREATE_FLAG (wmiutils.h)
description: Contains flags specifying the type of paths accepted.
helpviewer_keywords: ["WBEMPATH_CREATE_ACCEPT_ABSOLUTE","WBEMPATH_CREATE_ACCEPT_ALL","WBEMPATH_CREATE_ACCEPT_RELATIVE","WBEMPATH_TREAT_SINGLE_IDENT_AS_NS","tag_WBEM_PATH_CREATE_FLAG","tag_WBEM_PATH_CREATE_FLAG enumeration [Windows Management Instrumentation]","wmi.tag_wbem_path_create_flag","wmiutils/WBEMPATH_CREATE_ACCEPT_ABSOLUTE","wmiutils/WBEMPATH_CREATE_ACCEPT_ALL","wmiutils/WBEMPATH_CREATE_ACCEPT_RELATIVE","wmiutils/WBEMPATH_TREAT_SINGLE_IDENT_AS_NS","wmiutils/tag_WBEM_PATH_CREATE_FLAG"]
old-location: wmi\tag_wbem_path_create_flag.htm
tech.root: wmi
ms.assetid: d03d3e75-8e51-4cb8-a587-184dc89cc427
ms.date: 12/05/2018
ms.keywords: WBEMPATH_CREATE_ACCEPT_ABSOLUTE, WBEMPATH_CREATE_ACCEPT_ALL, WBEMPATH_CREATE_ACCEPT_RELATIVE, WBEMPATH_TREAT_SINGLE_IDENT_AS_NS, tag_WBEM_PATH_CREATE_FLAG, tag_WBEM_PATH_CREATE_FLAG enumeration [Windows Management Instrumentation], wmi.tag_wbem_path_create_flag, wmiutils/WBEMPATH_CREATE_ACCEPT_ABSOLUTE, wmiutils/WBEMPATH_CREATE_ACCEPT_ALL, wmiutils/WBEMPATH_CREATE_ACCEPT_RELATIVE, wmiutils/WBEMPATH_TREAT_SINGLE_IDENT_AS_NS, wmiutils/tag_WBEM_PATH_CREATE_FLAG
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
req.typenames: tag_WBEM_PATH_CREATE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_PATH_CREATE_FLAG
 - wmiutils/tag_WBEM_PATH_CREATE_FLAG
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
 - tag_WBEM_PATH_CREATE_FLAG
---

# tag_WBEM_PATH_CREATE_FLAG enumeration


## -description

Contains flags specifying the type of paths accepted.

## -enum-fields

### -field WBEMPATH_CREATE_ACCEPT_RELATIVE:0x1

Allow paths without server names.

### -field WBEMPATH_CREATE_ACCEPT_ABSOLUTE:0x2

Reserved for future use.

### -field WBEMPATH_CREATE_ACCEPT_ALL:0x4

Allow setting an empty path (which additionally clears out the object), Also allows paths which have just the server names, or paths which don't have server names.

### -field WBEMPATH_TREAT_SINGLE_IDENT_AS_NS:0x8

A simple path, such as "XYZ" is interpreted as a namespace.

