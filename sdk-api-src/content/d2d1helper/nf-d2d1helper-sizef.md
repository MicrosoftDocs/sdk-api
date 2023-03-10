---
UID: NF:d2d1helper.SizeF
title: SizeF function (d2d1helper.h)
description: Creates a D2D1_SIZE_F structure that contains the specified width and height.
helpviewer_keywords: ["SizeF","SizeF function [Direct2D]","d2d1helper/SizeF","direct2d.sizef"]
old-location: direct2d\sizef.htm
tech.root: Direct2D
ms.assetid: dbb75605-a0ec-464c-bb10-4455a90c4ae9
ms.date: 12/05/2018
ms.keywords: SizeF, SizeF function [Direct2D], d2d1helper/SizeF, direct2d.sizef
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
 - SizeF
 - d2d1helper/SizeF
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
 - SizeF
---

# SizeF function


## -description

Creates a <a href="/windows/desktop/Direct2D/d2d1-size-f">D2D1_SIZE_F</a> structure that contains the specified width and height.

## -parameters

### -param width

Type: <b>FLOAT</b>

The width of the size. The default value is 0.f.

### -param height

Type: <b>FLOAT</b>

The height of the size. The default value is 0.f.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-size-f">D2D1_SIZE_F</a></b>

The new size structure.