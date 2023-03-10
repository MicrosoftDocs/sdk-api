---
UID: NF:tom.ITextFont.IsEqual
title: ITextFont::IsEqual (tom.h)
description: Determines whether this text font object has the same properties as the specified text font object. (ITextFont.IsEqual)
helpviewer_keywords: ["ITextFont interface [Windows Controls]","IsEqual method","ITextFont.IsEqual","ITextFont::IsEqual","IsEqual","IsEqual method [Windows Controls]","IsEqual method [Windows Controls]","ITextFont interface","_win32_ITextFont_IsEqual","_win32_ITextFont_IsEqual_cpp","controls.ITextFont_IsEqual","controls._win32_ITextFont_IsEqual","tom/ITextFont::IsEqual"]
old-location: controls\ITextFont_IsEqual.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontisequal.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],IsEqual method, ITextFont.IsEqual, ITextFont::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextFont interface, _win32_ITextFont_IsEqual, _win32_ITextFont_IsEqual_cpp, controls.ITextFont_IsEqual, controls._win32_ITextFont_IsEqual, tom/ITextFont::IsEqual
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITextFont::IsEqual
 - tom/ITextFont::IsEqual
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
 - ITextFont.IsEqual
---

# ITextFont::IsEqual


## -description

Determines whether this text font object has the same properties as the specified text font object.

## -parameters

### -param pFont

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>*</b>

The text font object to compare against.

### -param pValue

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the font objects have the same properties or <b>tomFalse</b> if they do not. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If the text font objects have the same properties, the method succeeds and returns <b>S_OK</b>. If the text font objects do not have the same properties, the method fails and returns <b>S_FALSE</b>. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

The text font objects are equal only if <i>pFont</i> belongs to the same Text Object Model (TOM) object as the current font object. The <b>ITextFont::IsEqual</b> method ignores entries for which either font object has an <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUndefined</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
