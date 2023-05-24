---
UID: NF:tom.ITextFont2.IsEqual2
title: ITextFont2::IsEqual2 (tom.h)
description: Determines whether this text font object has the same properties as the specified text font object. (ITextFont2.IsEqual2)
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","IsEqual2 method","ITextFont2.IsEqual2","ITextFont2::IsEqual2","IsEqual2","IsEqual2 method [Windows Controls]","IsEqual2 method [Windows Controls]","ITextFont2 interface","controls.itextfont2_isequal2","tom/ITextFont2::IsEqual2"]
old-location: controls\itextfont2_isequal2.htm
tech.root: Controls
ms.assetid: c423bbdb-a108-4f29-8dc4-3dd35849f39a
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],IsEqual2 method, ITextFont2.IsEqual2, ITextFont2::IsEqual2, IsEqual2, IsEqual2 method [Windows Controls], IsEqual2 method [Windows Controls],ITextFont2 interface, controls.itextfont2_isequal2, tom/ITextFont2::IsEqual2
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
 - ITextFont2::IsEqual2
 - tom/ITextFont2::IsEqual2
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
 - ITextFont2.IsEqual2
---

# ITextFont2::IsEqual2


## -description

Determines whether this text font object has the same properties as the specified text font object.

## -parameters

### -param pFont [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>*</b>

The text font object to compare against.

### -param pB [out]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-rich-edit-controls">tomBool</a> value that is <b>tomTrue</b> if the font objects have the same properties, or <b>tomFalse</b> if they don't. This parameter can be <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 For two text font objects to be equal, both must belong to the same Text Object Model (TOM) object. 

The <b>ITextFont::IsEqual2</b> method ignores entries for which either font object has a <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUndefined</a> value.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-isequal">ITextFont::IsEqual</a>
