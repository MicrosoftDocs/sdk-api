---
UID: NE:wmiutils.tag_WBEM_PATH_CREATE_FLAG
title: tag_WBEM_PATH_CREATE_FLAG
author: windows-sdk-content
description: Contains flags specifying the type of paths accepted.
old-location: wmi\tag_wbem_path_create_flag.htm
old-project: WmiSdk
ms.assetid: d03d3e75-8e51-4cb8-a587-184dc89cc427
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WBEMPATH_CREATE_ACCEPT_ABSOLUTE, WBEMPATH_CREATE_ACCEPT_ALL, WBEMPATH_CREATE_ACCEPT_RELATIVE, WBEMPATH_TREAT_SINGLE_IDENT_AS_NS, tag_WBEM_PATH_CREATE_FLAG, tag_WBEM_PATH_CREATE_FLAG enumeration [Windows Management Instrumentation], wmi.tag_wbem_path_create_flag, wmiutils/WBEMPATH_CREATE_ACCEPT_ABSOLUTE, wmiutils/WBEMPATH_CREATE_ACCEPT_ALL, wmiutils/WBEMPATH_CREATE_ACCEPT_RELATIVE, wmiutils/WBEMPATH_TREAT_SINGLE_IDENT_AS_NS, wmiutils/tag_WBEM_PATH_CREATE_FLAG
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
tech.root: 
req.typenames: tag_WBEM_PATH_CREATE_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WMIUtils.h
api_name:
 - tag_WBEM_PATH_CREATE_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tag_WBEM_PATH_CREATE_FLAG enumeration


## -description


Contains flags specifying the type of paths accepted.


## -enum-fields




### -field WBEMPATH_CREATE_ACCEPT_RELATIVE

Allow paths without server names.


### -field WBEMPATH_CREATE_ACCEPT_ABSOLUTE

Reserved for future use.


### -field WBEMPATH_CREATE_ACCEPT_ALL

Allow setting an empty path (which additionally clears out the object), Also allows paths which have just the server names, or paths which don't have server names.


### -field WBEMPATH_TREAT_SINGLE_IDENT_AS_NS

A simple path, such as "XYZ" is interpreted as a namespace.

