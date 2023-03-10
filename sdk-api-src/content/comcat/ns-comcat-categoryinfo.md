---
UID: NS:comcat.tagCATEGORYINFO
title: CATEGORYINFO (comcat.h)
description: Describes a component category.
helpviewer_keywords: ["*LPCATEGORYINFO","CATEGORYINFO","CATEGORYINFO structure [COM]","_com_categoryinfo_structure","com.categoryinfo","comcat/CATEGORYINFO"]
old-location: com\categoryinfo.htm
tech.root: com
ms.assetid: a5f0cb04-595d-4388-8943-79b9da76022b
ms.date: 12/05/2018
ms.keywords: '*LPCATEGORYINFO, CATEGORYINFO, CATEGORYINFO structure [COM], _com_categoryinfo_structure, com.categoryinfo, comcat/CATEGORYINFO'
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
targetos: Windows
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCATEGORYINFO
 - comcat/tagCATEGORYINFO
 - LPCATEGORYINFO
 - comcat/LPCATEGORYINFO
 - CATEGORYINFO
 - comcat/CATEGORYINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Comcat.h
api_name:
 - CATEGORYINFO
---

# CATEGORYINFO structure


## -description

Describes a component category.

## -struct-fields

### -field catid

The category identifier for the component.

### -field lcid

The locale identifier. See <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

### -field szDescription

The description of the category (cannot exceed 128 characters).

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatregister">ICatRegister</a>