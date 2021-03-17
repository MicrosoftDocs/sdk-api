---
UID: NF:tom.ITextFont.CanChange
title: ITextFont::CanChange (tom.h)
description: Determines whether the font can be changed.
helpviewer_keywords: ["CanChange","CanChange method [Windows Controls]","CanChange method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","CanChange method","ITextFont.CanChange","ITextFont::CanChange","_win32_ITextFont_CanChange","_win32_ITextFont_CanChange_cpp","controls.ITextFont_CanChange","controls._win32_ITextFont_CanChange","tom/ITextFont::CanChange"]
old-location: controls\ITextFont_CanChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontcanchange.htm
ms.date: 12/05/2018
ms.keywords: CanChange, CanChange method [Windows Controls], CanChange method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],CanChange method, ITextFont.CanChange, ITextFont::CanChange, _win32_ITextFont_CanChange, _win32_ITextFont_CanChange_cpp, controls.ITextFont_CanChange, controls._win32_ITextFont_CanChange, tom/ITextFont::CanChange
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
 - ITextFont::CanChange
 - tom/ITextFont::CanChange
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
 - ITextFont.CanChange
---

# ITextFont::CanChange


## -description

Determines whether the font can be changed.

## -parameters

### -param pValue [retval]

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the font can be changed or <b>tomFalse</b> if it cannot be changed. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If the font can change, the method returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font cannot change.

</td>
</tr>
</table>

## -remarks

The *<i>pbCanChange</i> returns <b>tomTrue</b> only if the font can be changed. That is, no part of an associated range is protected and an associated document is not read-only. If this <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> object is a duplicate, no protection rules apply.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>