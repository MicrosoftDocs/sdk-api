---
UID: NF:tom.ITextFont.GetStyle
title: ITextFont::GetStyle (tom.h)
description: Gets the character style handle of the characters in a range.
helpviewer_keywords: ["GetStyle","GetStyle method [Windows Controls]","GetStyle method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetStyle method","ITextFont.GetStyle","ITextFont::GetStyle","_win32_ITextFont_GetStyle","_win32_ITextFont_GetStyle_cpp","controls.ITextFont_GetStyle","controls._win32_ITextFont_GetStyle","tom/ITextFont::GetStyle"]
old-location: controls\ITextFont_GetStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontgetstyle.htm
ms.date: 12/05/2018
ms.keywords: GetStyle, GetStyle method [Windows Controls], GetStyle method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetStyle method, ITextFont.GetStyle, ITextFont::GetStyle, _win32_ITextFont_GetStyle, _win32_ITextFont_GetStyle_cpp, controls.ITextFont_GetStyle, controls._win32_ITextFont_GetStyle, tom/ITextFont::GetStyle
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
 - ITextFont::GetStyle
 - tom/ITextFont::GetStyle
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
 - ITextFont.GetStyle
---

# ITextFont::GetStyle


## -description

Gets the character style handle of the characters in a range.

## -parameters

### -param pValue

Type: <b>long*</b>

The character style handle.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.

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
The font object is attached to a range that was deleted.

</td>
</tr>
</table>
 

For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

The Text Object Model (TOM) version 1.0 does not specify the meanings of the style handles. The meanings depend on other facilities of the text system that implements TOM.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setstyle">SetStyle</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>