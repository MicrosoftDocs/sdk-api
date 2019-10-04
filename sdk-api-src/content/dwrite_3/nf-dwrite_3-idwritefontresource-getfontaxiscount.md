---
UID: NF:dwrite_3.IDWriteFontResource.GetFontAxisCount
title: IDWriteFontResource::GetFontAxisCount
author: windows-sdk-content
description: Retrieves the number of axes supported by the font resource.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetFontAxisCount method, IDWriteFontResource.GetFontAxisCount, IDWriteFontResource::GetFontAxisCount, GetFontAxisCount, GetFontAxisCount method [Direct Write], GetFontAxisCount method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getfontaxiscount, dwrite_3/IDWriteFontResource::GetFontAxisCount
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontResource.GetFontAxisCount"
dev_langs:
 - c++
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontResource::GetFontAxisCount
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the number of axes supported by the font resource. This includes both static and variable axes (see [DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)).

## -returns

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of axes defined by the font face.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
