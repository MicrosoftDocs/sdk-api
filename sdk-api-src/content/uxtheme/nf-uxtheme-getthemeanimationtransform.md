---
UID: NF:uxtheme.GetThemeAnimationTransform
title: GetThemeAnimationTransform function (uxtheme.h)
description: Gets an animation transform operation based on storyboard id, target id and transform index.
helpviewer_keywords: ["GetThemeAnimationTransform","GetThemeAnimationTransform function [Windows Controls]","controls.getthemeanimationtransform","uxtheme/GetThemeAnimationTransform"]
old-location: controls\getthemeanimationtransform.htm
tech.root: Controls
ms.assetid: 3B7691C0-4237-4CE4-9B7C-937089AC5606
ms.date: 12/05/2018
ms.keywords: GetThemeAnimationTransform, GetThemeAnimationTransform function [Windows Controls], controls.getthemeanimationtransform, uxtheme/GetThemeAnimationTransform
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeAnimationTransform
 - uxtheme/GetThemeAnimationTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeAnimationTransform
---

# GetThemeAnimationTransform function


## -description

Gets an animation transform operation
based on storyboard id, target id and transform
index.

## -parameters

### -param hTheme [in]

An opened theme handle.

### -param iStoryboardId [in]

A predefined storyboard identifier.

### -param iTargetId [in]

A predefined target identifier.

### -param dwTransformIndex [in]

The zero-based index of a transform operation.

### -param pTransform [out]

A pointer to a buffer to receive a transform structure.

### -param cbSize [in]

The byte size of the buffer pointed by <i>pTransform</i>.

### -param pcbSizeOut [out]

The                                    byte  size of a transform operation structure.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

