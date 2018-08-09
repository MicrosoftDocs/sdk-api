---
UID: NS:comcat.tagCATEGORYINFO
title: tagCATEGORYINFO
author: windows-sdk-content
description: Describes a component category.
old-location: com\categoryinfo.htm
old-project: com
ms.assetid: a5f0cb04-595d-4388-8943-79b9da76022b
ms.author: windowssdkdev
ms.date: 08/06/2018
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
req.idl: ComCat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
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
req.lib: 
req.dll: 
req.irql: 
---

# tagCATEGORYINFO structure


## -description


Describes a component category.



## -struct-fields




### -field catid

The category identifier for the component.


### -field lcid

The locale identifier. See <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.


### -field szDescription

The description of the category (cannot exceed 128 characters).


## -see-also




<a href="https://msdn.microsoft.com/3f4f9beb-51db-407f-91ea-6e32ff5796ce">ICatRegister</a>
 

 

