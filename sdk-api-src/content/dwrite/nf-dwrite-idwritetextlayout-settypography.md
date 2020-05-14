---
UID: NF:dwrite.IDWriteTextLayout.SetTypography
title: IDWriteTextLayout::SetTypography (dwrite.h)
description: Sets font typography features for text within a specified text range.helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetTypography method","IDWriteTextLayout.SetTypography","IDWriteTextLayout::SetTypography","SetTypography","SetTypography method [Direct Write]","SetTypography method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetTypography","dwrite/IDWriteTextLayout::SetTypography"]
old-location: directwrite\IDWriteTextLayout_SetTypography.htm
tech.root: DirectWrite
ms.assetid: ee0702fb-a3ff-442b-bd3b-6ff35fcba0ec
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetTypography method, IDWriteTextLayout.SetTypography, IDWriteTextLayout::SetTypography, SetTypography, SetTypography method [Direct Write], SetTypography method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetTypography, dwrite/IDWriteTextLayout::SetTypography
f1_keywords:
- dwrite/IDWriteTextLayout.SetTypography
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteTextLayout.SetTypography
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout::SetTypography


## -description


 Sets  font typography features for text within a specified text range.


## -parameters




### -param typography

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a>*</b>

Pointer to font typography settings. 


### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>
 

 

