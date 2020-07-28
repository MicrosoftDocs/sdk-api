---
UID: NF:dwrite_3.IDWriteTextFormat2.GetLineSpacing
title: IDWriteTextFormat2::GetLineSpacing (dwrite_3.h)
description: Gets the line spacing adjustment set for a multiline text paragraph.
helpviewer_keywords: ["GetLineSpacing","GetLineSpacing method [Direct Write]","GetLineSpacing method [Direct Write]","IDWriteTextFormat2 interface","IDWriteTextFormat2 interface [Direct Write]","GetLineSpacing method","IDWriteTextFormat2.GetLineSpacing","IDWriteTextFormat2::GetLineSpacing","directwrite.idwritetextformat2_getlinespacing","dwrite_3/IDWriteTextFormat2::GetLineSpacing"]
old-location: directwrite\idwritetextformat2_getlinespacing.htm
tech.root: DirectWrite
ms.assetid: 1e05687f-137e-06f8-b9c8-983f434f7578
ms.date: 12/05/2018
ms.keywords: GetLineSpacing, GetLineSpacing method [Direct Write], GetLineSpacing method [Direct Write],IDWriteTextFormat2 interface, IDWriteTextFormat2 interface [Direct Write],GetLineSpacing method, IDWriteTextFormat2.GetLineSpacing, IDWriteTextFormat2::GetLineSpacing, directwrite.idwritetextformat2_getlinespacing, dwrite_3/IDWriteTextFormat2::GetLineSpacing
f1_keywords:
- dwrite_3/IDWriteTextFormat2.GetLineSpacing
dev_langs:
- c++
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteTextFormat2.GetLineSpacing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextFormat2::GetLineSpacing


## -description


Gets the line spacing adjustment set for a multiline text paragraph.


## -parameters




### -param lineSpacingOptions [out]

Type: <b><a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing">DWRITE_LINE_SPACING</a>*</b>

A structure describing how the space between lines is managed for the paragraph.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/DirectWrite/idwritetextformat2">IDWriteTextFormat2</a>
 

 

