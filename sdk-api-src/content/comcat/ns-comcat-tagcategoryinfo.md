---
UID: NS:comcat.tagCATEGORYINFO
title: tagCATEGORYINFO
author: windows-sdk-content
description: Describes a component category.
old-location: com\categoryinfo.htm
tech.root: com
ms.assetid: a5f0cb04-595d-4388-8943-79b9da76022b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPCATEGORYINFO, CATEGORYINFO, CATEGORYINFO structure [COM], _com_categoryinfo_structure, com.categoryinfo, comcat/CATEGORYINFO, tagCATEGORYINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Comcat.h
api_name:
 - CATEGORYINFO
product: Windows
targetos: Windows
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
req.redist: 
---

# tagCATEGORYINFO structure


## -description


Describes a component category.



## -struct-fields




### -field catid

The category identifier for the component.


### -field lcid

The locale identifier. See <a href="https://msdn.microsoft.com/en-us/library/Dd318693(v=VS.85).aspx">Language Identifier Constants and Strings</a>.


### -field szDescription

The description of the category (cannot exceed 128 characters).


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680737(v=VS.85).aspx">ICatRegister</a>
 

 

