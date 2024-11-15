---
UID: NF:dwrite_3.IDWriteFontResource.GetAxisValueNameCount
title: IDWriteFontResource::GetAxisValueNameCount
description: Retrieves the number of named values for a specific axis.
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","GetAxisValueNameCount method","IDWriteFontResource.GetAxisValueNameCount","IDWriteFontResource::GetAxisValueNameCount","GetAxisValueNameCount","GetAxisValueNameCount method [Direct Write]","GetAxisValueNameCount method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_getaxisvaluenamecount","dwrite_3/IDWriteFontResource::GetAxisValueNameCount"]
tech.root: DirectWrite
ms.date: 09/15/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetAxisValueNameCount method, IDWriteFontResource.GetAxisValueNameCount, IDWriteFontResource::GetAxisValueNameCount, GetAxisValueNameCount, GetAxisValueNameCount method [Direct Write], GetAxisValueNameCount method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getaxisvaluenamecount, dwrite_3/IDWriteFontResource::GetAxisValueNameCount
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFontResource::GetAxisValueNameCount
 - dwrite_3/IDWriteFontResource::GetAxisValueNameCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontResource::GetAxisValueNameCount
---

## -description

Retrieves the number of named values for a specific axis.

## -parameters

### -param axisIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Font axis, from 0 to [GetFontAxisCount](./nf-dwrite_3-idwritefontresource-getfontaxiscount.md) minus 1.

## -returns

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of named values for the axis specified by *axisIndex*.

## -remarks

## -see-also
