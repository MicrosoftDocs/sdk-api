---
UID: NF:tom.ITextFont.SetSpacing
title: ITextFont::SetSpacing (tom.h)
description: Sets the amount of horizontal spacing between characters.
helpviewer_keywords: ["ITextFont interface [Windows Controls]","SetSpacing method","ITextFont.SetSpacing","ITextFont::SetSpacing","SetSpacing","SetSpacing method [Windows Controls]","SetSpacing method [Windows Controls]","ITextFont interface","_win32_ITextFont_SetSpacing","_win32_ITextFont_SetSpacing_cpp","controls.ITextFont_SetSpacing","controls._win32_ITextFont_SetSpacing","tom/ITextFont::SetSpacing"]
old-location: controls\ITextFont_SetSpacing.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setspacing.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],SetSpacing method, ITextFont.SetSpacing, ITextFont::SetSpacing, SetSpacing, SetSpacing method [Windows Controls], SetSpacing method [Windows Controls],ITextFont interface, _win32_ITextFont_SetSpacing, _win32_ITextFont_SetSpacing_cpp, controls.ITextFont_SetSpacing, controls._win32_ITextFont_SetSpacing, tom/ITextFont::SetSpacing
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
 - ITextFont::SetSpacing
 - tom/ITextFont::SetSpacing
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
 - ITextFont.SetSpacing
---

# ITextFont::SetSpacing


## -description

Sets the amount of horizontal spacing between characters.

## -parameters

### -param Value [in]

Type: <b>float</b>

The new amount of horizontal spacing between characters, in floating-point points.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -remarks

Displayed text typically has an intercharacter spacing value of zero. Positive values expand the spacing, and negative values compress it.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-getspacing">GetSpacing</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>