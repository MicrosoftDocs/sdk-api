---
UID: NF:ocidl.IFont.SetRatio
title: IFont::SetRatio (ocidl.h)
description: Converts the scaling factor for this font between logical units and HIMETRIC units.
helpviewer_keywords: ["IFont interface [COM]","SetRatio method","IFont.SetRatio","IFont::SetRatio","SetRatio","SetRatio method [COM]","SetRatio method [COM]","IFont interface","_ctrl_ifont_setratio","com.ifont_setratio","ocidl/IFont::SetRatio"]
old-location: com\ifont_setratio.htm
tech.root: com
ms.assetid: aaa962d8-6f7f-4031-aa10-09cadf0e5aec
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],SetRatio method, IFont.SetRatio, IFont::SetRatio, SetRatio, SetRatio method [COM], SetRatio method [COM],IFont interface, _ctrl_ifont_setratio, com.ifont_setratio, ocidl/IFont::SetRatio
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFont::SetRatio
 - ocidl/IFont::SetRatio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.SetRatio
---

# IFont::SetRatio


## -description

Converts the scaling factor for this font between logical units and <b>HIMETRIC</b> units. 
    <b>HIMETRIC</b> units are used to express the point size in the 
    <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_size">IFont::get_Size</a> and 
    <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_size">IFont::put_Size</a> methods. The values passed to 
    <b>IFont::SetRatio</b> are used to compute the display size of 
    the font in logical units from the value in the <b>Size</b> property:

<code>Display Size = ( cyLogical / cyHimetric ) * Size</code>

## -parameters

### -param cyLogical [in]

The font size, in logical units.

### -param cyHimetric [in]

The font size, in <b>HIMETRIC</b> units.

## -returns

The method supports the standard return values E_UNEXPECTED, E_INVALIDARG, and S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_size">IFont::get_Size</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_size">IFont::put_Size</a>