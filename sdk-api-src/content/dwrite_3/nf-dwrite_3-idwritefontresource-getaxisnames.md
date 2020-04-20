---
UID: NF:dwrite_3.IDWriteFontResource.GetAxisNames
title: IDWriteFontResource::GetAxisNames
description: Retrieves the localized names of a font axis.helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","GetAxisNames method","IDWriteFontResource.GetAxisNames","IDWriteFontResource::GetAxisNames","GetAxisNames","GetAxisNames method [Direct Write]","GetAxisNames method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_getaxisnames","dwrite_3/IDWriteFontResource::GetAxisNames"]
tech.root: DirectWrite
ms.date: 09/13/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetAxisNames method, IDWriteFontResource.GetAxisNames, IDWriteFontResource::GetAxisNames, GetAxisNames, GetAxisNames method [Direct Write], GetAxisNames method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getaxisnames, dwrite_3/IDWriteFontResource::GetAxisNames
f1_keywords:
- dwrite_3/IDWriteFontResource.GetAxisNames
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
- IDWriteFontResource::GetAxisNames
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the localized names of a font axis.

## -parameters

### -param axisIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Font axis, from 0 to [GetFontAxisCount](/windows/win32/api/dwrite/nf-dwrite_3-idwritefontresource-getfontaxiscount) minus 1.

### -param names

Type: **[IDWriteLocalizedStrings](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings)\*\***

The address of a pointer to an [IDWriteLocalizedStrings](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) interface. On successful completion, the function sets the pointer to a newly created localized strings object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

The font author may not have supplied names for some font axes. The localized strings will be empty in that case.

## -see-also
