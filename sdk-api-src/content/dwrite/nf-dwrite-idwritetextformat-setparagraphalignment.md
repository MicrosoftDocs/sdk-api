---
UID: NF:dwrite.IDWriteTextFormat.SetParagraphAlignment
title: IDWriteTextFormat::SetParagraphAlignment (dwrite.h)
description: Sets the alignment option of a paragraph relative to the layout box's top and bottom edge.
helpviewer_keywords: ["IDWriteTextFormat interface [Direct Write]","SetParagraphAlignment method","IDWriteTextFormat.SetParagraphAlignment","IDWriteTextFormat::SetParagraphAlignment","SetParagraphAlignment","SetParagraphAlignment method [Direct Write]","SetParagraphAlignment method [Direct Write]","IDWriteTextFormat interface","directwrite.IDWriteTextFormat_SetParagraphAlignment","dwrite/IDWriteTextFormat::SetParagraphAlignment"]
old-location: directwrite\IDWriteTextFormat_SetParagraphAlignment.htm
tech.root: DirectWrite
ms.assetid: a6eb8aea-3945-471d-a34a-c2f3221dfeaf
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetParagraphAlignment method, IDWriteTextFormat.SetParagraphAlignment, IDWriteTextFormat::SetParagraphAlignment, SetParagraphAlignment, SetParagraphAlignment method [Direct Write], SetParagraphAlignment method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetParagraphAlignment, dwrite/IDWriteTextFormat::SetParagraphAlignment
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextFormat::SetParagraphAlignment
 - dwrite/IDWriteTextFormat::SetParagraphAlignment
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
 - IDWriteTextFormat.SetParagraphAlignment
---

# IDWriteTextFormat::SetParagraphAlignment


## -description

 Sets the alignment option of a paragraph relative to the layout box's top and bottom edge.

## -parameters

### -param paragraphAlignment

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment">DWRITE_PARAGRAPH_ALIGNMENT</a></b>

The paragraph alignment option being set for a paragraph; see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment">DWRITE_PARAGRAPH_ALIGNMENT</a> for more information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

