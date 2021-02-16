---
UID: NF:tom.ITextFont2.SetPositionSubSuper
title: ITextFont2::SetPositionSubSuper (tom.h)
description: Sets the position of a subscript or superscript relative to the baseline, as a percentage of the font height.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetPositionSubSuper method","ITextFont2.SetPositionSubSuper","ITextFont2::SetPositionSubSuper","SetPositionSubSuper","SetPositionSubSuper method [Windows Controls]","SetPositionSubSuper method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setpositionsubsuper","tom/ITextFont2::SetPositionSubSuper"]
old-location: controls\itextfont2_setpositionsubsuper.htm
tech.root: Controls
ms.assetid: 3f78a91b-17a3-48ff-9ca0-1eb4f9c95be4
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetPositionSubSuper method, ITextFont2.SetPositionSubSuper, ITextFont2::SetPositionSubSuper, SetPositionSubSuper, SetPositionSubSuper method [Windows Controls], SetPositionSubSuper method [Windows Controls],ITextFont2 interface, controls.itextfont2_setpositionsubsuper, tom/ITextFont2::SetPositionSubSuper
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont2::SetPositionSubSuper
 - tom/ITextFont2::SetPositionSubSuper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.SetPositionSubSuper
---

# ITextFont2::SetPositionSubSuper


## -description

Sets the position of a subscript or superscript relative to the baseline, as a percentage of the font height.

## -parameters

### -param Value [in]

Type: <b>long</b>

The new subscript or superscript position.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getpositionsubsuper">ITextFont2::GetPositionSubSuper</a>