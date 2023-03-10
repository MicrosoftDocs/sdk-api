---
UID: NS:uxtheme._INTLIST
title: INTLIST (uxtheme.h)
description: Contains an array or list of int data items from a visual style.
helpviewer_keywords: ["*PINTLIST","INTLIST","INTLIST structure [Windows Controls]","PINTLIST","PINTLIST structure pointer [Windows Controls]","controls.INTLIST","controls.inet_INTLIST","inet_INTLIST","inet_INTLIST_cpp","uxtheme/INTLIST","uxtheme/PINTLIST"]
old-location: controls\INTLIST.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\intlist.htm
ms.date: 12/05/2018
ms.keywords: '*PINTLIST, INTLIST, INTLIST structure [Windows Controls], PINTLIST, PINTLIST structure pointer [Windows Controls], controls.INTLIST, controls.inet_INTLIST, inet_INTLIST, inet_INTLIST_cpp, uxtheme/INTLIST, uxtheme/PINTLIST'
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: INTLIST, *PINTLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTLIST
 - uxtheme/_INTLIST
 - PINTLIST
 - uxtheme/PINTLIST
 - INTLIST
 - uxtheme/INTLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UxTheme.h
api_name:
 - INTLIST
---

# INTLIST structure


## -description

Contains an array or list of <b>int</b> data items from a visual style.

## -struct-fields

### -field iValueCount

Type: <b>int</b>

Number of values in the list.

### -field iValues

Type: <b>int[MAX_INTLIST_COUNT]</b>

List of integers. The constant MAX_INTLIST_COUNT, by definition, is equal to 402 under Windows Vista, but only 10 under earlier versions of Windows.

## -remarks

The lists are returned by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemeintlist">GetThemeIntList</a>.