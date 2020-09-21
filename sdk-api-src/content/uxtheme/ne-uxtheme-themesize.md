---
UID: NE:uxtheme.THEMESIZE
title: THEMESIZE (uxtheme.h)
description: Identifies the type of size value to retrieve for a visual style part.
helpviewer_keywords: ["THEMESIZE","THEMESIZE enumeration [Windows Controls]","THEME_SIZE","THEME_SIZE enumeration [Windows Controls]","TS_DRAW","TS_MIN","TS_TRUE","controls.THEME_SIZE","controls.inet_THEME_SIZE","inet_THEME_SIZE","inet_THEME_SIZE_cpp","uxtheme/THEMESIZE","uxtheme/TS_DRAW","uxtheme/TS_MIN","uxtheme/TS_TRUE"]
old-location: controls\THEME_SIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\enums\themesize.htm
ms.date: 12/05/2018
ms.keywords: THEMESIZE, THEMESIZE enumeration [Windows Controls], THEME_SIZE, THEME_SIZE enumeration [Windows Controls], TS_DRAW, TS_MIN, TS_TRUE, controls.THEME_SIZE, controls.inet_THEME_SIZE, inet_THEME_SIZE, inet_THEME_SIZE_cpp, uxtheme/THEMESIZE, uxtheme/TS_DRAW, uxtheme/TS_MIN, uxtheme/TS_TRUE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - THEMESIZE
 - uxtheme/THEMESIZE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - THEME_SIZE
---

# THEMESIZE enumeration


## -description

Identifies the type of size value to retrieve for a visual style part.

## -enum-fields

### -field TS_MIN

Receives the minimum size of a visual style part.

### -field TS_TRUE

Receives the size of the visual style part that will best fit the available space.

### -field TS_DRAW

Receives the size that the theme manager uses to draw a part.

## -remarks

A value from the <b>THEMESIZE</b> enumeration is used with the <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemepartsize">GetThemePartSize</a> function to specify the type of size value to retrieve for a particular visual style part.