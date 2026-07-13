---
UID: NF:dwrite_3.IDWriteFontFaceReference.CreateFontFaceWithSimulations
title: IDWriteFontFaceReference::CreateFontFaceWithSimulations (dwrite_3.h)
description: Creates a font face with alternate font simulations, for example, to explicitly simulate a bold font face out of a regular variant.
helpviewer_keywords: ["CreateFontFaceWithSimulations","CreateFontFaceWithSimulations method [Direct Write]","CreateFontFaceWithSimulations method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","CreateFontFaceWithSimulations method","IDWriteFontFaceReference.CreateFontFaceWithSimulations","IDWriteFontFaceReference::CreateFontFaceWithSimulations","directwrite.idwritefontfacereference_createfontfacewithsimulations","dwrite_3/IDWriteFontFaceReference::CreateFontFaceWithSimulations"]
old-location: directwrite\idwritefontfacereference_createfontfacewithsimulations.htm
tech.root: DirectWrite
ms.assetid: 99b6fb24-2f66-8132-b66e-ca711bb0c7e0
ms.date: 09/10/2025
ms.keywords: CreateFontFaceWithSimulations, CreateFontFaceWithSimulations method [Direct Write], CreateFontFaceWithSimulations method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],CreateFontFaceWithSimulations method, IDWriteFontFaceReference.CreateFontFaceWithSimulations, IDWriteFontFaceReference::CreateFontFaceWithSimulations, directwrite.idwritefontfacereference_createfontfacewithsimulations, dwrite_3/IDWriteFontFaceReference::CreateFontFaceWithSimulations
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFaceReference::CreateFontFaceWithSimulations
 - dwrite_3/IDWriteFontFaceReference::CreateFontFaceWithSimulations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFaceReference.CreateFontFaceWithSimulations
---

# IDWriteFontFaceReference::CreateFontFaceWithSimulations


## -description

Creates a font face with alternate font simulations, for example, to explicitly simulate a bold font face out of a regular variant.

## -parameters

### -param fontFaceSimulationFlags

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations">DWRITE_FONT_SIMULATIONS</a></b>

Font face simulation flags for algorithmic emboldening and italicization.

### -param fontFace [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>**</b>

Newly created font face object, or nullptr in the case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function can fail with DWRITE_E_REMOTEFONT if the font is not local.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

