---
UID: NF:d2d1helper.SizeU
title: SizeU function (d2d1helper.h)
description: Creates a D2D1_SIZE_U structure that contains the specified width and height.
helpviewer_keywords: ["SizeU","SizeU function [Direct2D]","d2d1helper/SizeU","direct2d.sizeu"]
old-location: direct2d\sizeu.htm
tech.root: Direct2D
ms.assetid: 147670e3-c451-401e-9e79-dacd7c33385d
ms.date: 12/05/2018
ms.keywords: SizeU, SizeU function [Direct2D], d2d1helper/SizeU, direct2d.sizeu
req.header: d2d1helper.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SizeU
 - d2d1helper/SizeU
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - SizeU
---

# SizeU function


## -description

Creates a <a href="/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a> structure that contains the specified width and height.

## -parameters

### -param width

Type: <b>UINT32</b>

The width of the size. The default value is 0.

### -param height

Type: <b>UINT32</b>

The height of the size. The default value is 0.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The new size structure.