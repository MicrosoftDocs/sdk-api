---
UID: NE:dwrite.DWRITE_SCRIPT_SHAPES
title: DWRITE_SCRIPT_SHAPES (dwrite.h)
description: Indicates additional shaping requirements for text.
helpviewer_keywords: ["DWRITE_SCRIPT_SHAPES","DWRITE_SCRIPT_SHAPES enumeration [Direct Write]","DWRITE_SCRIPT_SHAPES_DEFAULT","DWRITE_SCRIPT_SHAPES_NO_VISUAL","directwrite.dwrite_script_shapes","dwrite/DWRITE_SCRIPT_SHAPES","dwrite/DWRITE_SCRIPT_SHAPES_DEFAULT","dwrite/DWRITE_SCRIPT_SHAPES_NO_VISUAL"]
old-location: directwrite\dwrite_script_shapes.htm
tech.root: DirectWrite
ms.assetid: 81ec0f3a-4dab-4497-893f-d791d9d9be6a
ms.date: 12/05/2018
ms.keywords: DWRITE_SCRIPT_SHAPES, DWRITE_SCRIPT_SHAPES enumeration [Direct Write], DWRITE_SCRIPT_SHAPES_DEFAULT, DWRITE_SCRIPT_SHAPES_NO_VISUAL, directwrite.dwrite_script_shapes, dwrite/DWRITE_SCRIPT_SHAPES, dwrite/DWRITE_SCRIPT_SHAPES_DEFAULT, dwrite/DWRITE_SCRIPT_SHAPES_NO_VISUAL
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_SCRIPT_SHAPES
 - dwrite/DWRITE_SCRIPT_SHAPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_SCRIPT_SHAPES
---

# DWRITE_SCRIPT_SHAPES enumeration


## -description

Indicates additional shaping requirements for text.

## -enum-fields

### -field DWRITE_SCRIPT_SHAPES_DEFAULT:0

Indicates that there is no additional shaping requirements for text. Text is shaped with the writing system default behavior.

### -field DWRITE_SCRIPT_SHAPES_NO_VISUAL:1

Indicates that text should leave no visible control or format control characters.

