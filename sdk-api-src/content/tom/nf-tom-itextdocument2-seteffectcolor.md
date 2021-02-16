---
UID: NF:tom.ITextDocument2.SetEffectColor
title: ITextDocument2::SetEffectColor (tom.h)
description: Specifies the color to use for special text attributes.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetEffectColor method","ITextDocument2.SetEffectColor","ITextDocument2::SetEffectColor","SetEffectColor","SetEffectColor method [Windows Controls]","SetEffectColor method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_seteffectcolor","tom/ITextDocument2::SetEffectColor"]
old-location: controls\itextdocument2_seteffectcolor.htm
tech.root: Controls
ms.assetid: 6371b525-96da-42a7-8cee-228b47208f46
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetEffectColor method, ITextDocument2.SetEffectColor, ITextDocument2::SetEffectColor, SetEffectColor, SetEffectColor method [Windows Controls], SetEffectColor method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_seteffectcolor, tom/ITextDocument2::SetEffectColor
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
 - ITextDocument2::SetEffectColor
 - tom/ITextDocument2::SetEffectColor
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
 - ITextDocument2.SetEffectColor
---

# ITextDocument2::SetEffectColor


## -description

Specifies the color to use for special text attributes.

## -parameters

### -param Index [in]

Type: <b>long</b>

The index of the color to retrieve. For a list of values, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-geteffectcolor">GetEffectColor</a>.

### -param Value [in]

Type: <b>long</b>

The new color for the specified index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The first 16 index values are for special underline colors. If an index between 1 and 16 hasn't been defined by a call to the <b>ITextDocument2:SetEffectColor</b> method, the corresponding Microsoft Word default color is used.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-geteffectcolor">ITextDocument2::GetEffectColor</a>