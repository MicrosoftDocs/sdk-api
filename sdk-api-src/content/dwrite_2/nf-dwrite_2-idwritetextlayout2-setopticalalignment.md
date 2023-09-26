---
UID: NF:dwrite_2.IDWriteTextLayout2.SetOpticalAlignment
title: IDWriteTextLayout2::SetOpticalAlignment (dwrite_2.h)
description: Set how the glyphs align to the edges the margin.
helpviewer_keywords: ["IDWriteTextLayout2 interface [Direct Write]","SetOpticalAlignment method","IDWriteTextLayout2.SetOpticalAlignment","IDWriteTextLayout2::SetOpticalAlignment","SetOpticalAlignment","SetOpticalAlignment method [Direct Write]","SetOpticalAlignment method [Direct Write]","IDWriteTextLayout2 interface","directwrite.idwritetextlayout2_setopticalalignment","dwrite_2/IDWriteTextLayout2::SetOpticalAlignment"]
old-location: directwrite\idwritetextlayout2_setopticalalignment.htm
tech.root: DirectWrite
ms.assetid: 10C9C3E7-4556-4848-A4CB-F822A689CAB0
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout2 interface [Direct Write],SetOpticalAlignment method, IDWriteTextLayout2.SetOpticalAlignment, IDWriteTextLayout2::SetOpticalAlignment, SetOpticalAlignment, SetOpticalAlignment method [Direct Write], SetOpticalAlignment method [Direct Write],IDWriteTextLayout2 interface, directwrite.idwritetextlayout2_setopticalalignment, dwrite_2/IDWriteTextLayout2::SetOpticalAlignment
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDWriteTextLayout2::SetOpticalAlignment
 - dwrite_2/IDWriteTextLayout2::SetOpticalAlignment
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
 - IDWriteTextLayout2.SetOpticalAlignment
---

# IDWriteTextLayout2::SetOpticalAlignment


## -description

Set how the glyphs align to the edges the margin.  Default behavior is to align glyphs using their default glyphs metrics, which include side bearings.

## -parameters

### -param opticalAlignment

Optical alignment option.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextlayout2">IDWriteTextLayout2</a>

