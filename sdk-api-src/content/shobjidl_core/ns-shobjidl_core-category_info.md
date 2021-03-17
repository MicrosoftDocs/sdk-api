---
UID: NS:shobjidl_core.CATEGORY_INFO
title: CATEGORY_INFO (shobjidl_core.h)
description: Contains category information. A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).
helpviewer_keywords: ["CATEGORY_INFO","CATEGORY_INFO structure [Windows Shell]","inet_CATEGORY_INFO","shell.CATEGORY_INFO","shobjidl_core/CATEGORY_INFO"]
old-location: shell\CATEGORY_INFO.htm
tech.root: shell
ms.assetid: 6198cd31-94db-4d31-9cc9-f8b90e661809
ms.date: 12/05/2018
ms.keywords: CATEGORY_INFO, CATEGORY_INFO structure [Windows Shell], inet_CATEGORY_INFO, shell.CATEGORY_INFO, shobjidl_core/CATEGORY_INFO
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CATEGORY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CATEGORY_INFO
 - shobjidl_core/CATEGORY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - CATEGORY_INFO
---

# CATEGORY_INFO structure


## -description

Contains category information. A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).

## -struct-fields

### -field cif

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags">CATEGORYINFO_FLAGS</a></b>

A flag from <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags">CATEGORYINFO_FLAGS</a> that specifies the type of information to retrieve.

### -field wszName

Type: <b>WCHAR[260]</b>

A character array that specifies the name of the category.