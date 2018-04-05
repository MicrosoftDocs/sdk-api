---
UID: NE:wmiutils.tag_WBEM_GET_TEXT_FLAGS
title: tag_WBEM_GET_TEXT_FLAGS
author: windows-driver-content
description: Contains flags which controls how the text is returned.
old-location: wmi\tag_wbem_get_text_flags.htm
old-project: WmiSdk
ms.assetid: 5b6cb2c0-d4e4-452b-840f-01fec2d57743
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: WBEMPATH_COMPRESSED, WBEMPATH_GET_NAMESPACE_ONLY, WBEMPATH_GET_ORIGINAL, WBEMPATH_GET_RELATIVE_ONLY, WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY, WBEMPATH_GET_SERVER_TOO, tag_WBEM_GET_TEXT_FLAGS, tag_WBEM_GET_TEXT_FLAGS enumeration [Windows Management Instrumentation], wmi.tag_wbem_get_text_flags, wmiutils/WBEMPATH_COMPRESSED, wmiutils/WBEMPATH_GET_NAMESPACE_ONLY, wmiutils/WBEMPATH_GET_ORIGINAL, wmiutils/WBEMPATH_GET_RELATIVE_ONLY, wmiutils/WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY, wmiutils/WBEMPATH_GET_SERVER_TOO, wmiutils/tag_WBEM_GET_TEXT_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: tag_WBEM_GET_TEXT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WMIUtils.h
api_name:
-	tag_WBEM_GET_TEXT_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tag_WBEM_GET_TEXT_FLAGS enumeration


## -description


Contains flags which controls how the text is returned.


## -enum-fields




### -field WBEMPATH_COMPRESSED

Obsolete. Do not use.


### -field WBEMPATH_GET_RELATIVE_ONLY

Returns the relative path, skips server and namespaces.


### -field WBEMPATH_GET_SERVER_TOO

Returns the entire path, including server and namespace.


### -field WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY

Returns only the server and namespace portion of the path. Ignores the class or key portion.


### -field WBEMPATH_GET_NAMESPACE_ONLY

Returns only the namespace portion of the path.


### -field WBEMPATH_GET_ORIGINAL

Returns whatever was passed in using 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a> method.

