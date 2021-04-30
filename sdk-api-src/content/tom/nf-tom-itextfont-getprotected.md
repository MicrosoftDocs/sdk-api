---
UID: NF:tom.ITextFont.GetProtected
title: ITextFont::GetProtected (tom.h)
description: Gets whether characters are protected against attempts to modify them.
helpviewer_keywords: ["GetProtected","GetProtected method [Windows Controls]","GetProtected method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetProtected method","ITextFont.GetProtected","ITextFont::GetProtected","_win32_ITextFont_GetProtected","_win32_ITextFont_GetProtected_cpp","controls.ITextFont_GetProtected","controls._win32_ITextFont_GetProtected","tom/ITextFont::GetProtected"]
old-location: controls\ITextFont_GetProtected.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getprotected.htm
ms.date: 12/05/2018
ms.keywords: GetProtected, GetProtected method [Windows Controls], GetProtected method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetProtected method, ITextFont.GetProtected, ITextFont::GetProtected, _win32_ITextFont_GetProtected, _win32_ITextFont_GetProtected_cpp, controls.ITextFont_GetProtected, controls._win32_ITextFont_GetProtected, tom/ITextFont::GetProtected
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
 - ITextFont::GetProtected
 - tom/ITextFont::GetProtected
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
 - ITextFont.GetProtected
---

# ITextFont::GetProtected


## -description

Gets whether characters are protected against attempts to modify them.

## -parameters

### -param pValue

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are protected.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not protected.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Protected property is undefined.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
</table>

## -remarks

In general, Text Object Model (TOM) methods that attempt to change the formatting or content of a range fail with <b>E_ACCESSDENIED</b> if any part of that range is protected, or if the document is read only. To make a change in protected text, the TOM client should attempt to turn off the protection of the text to be modified. The owner of the document may permit this to happen. For example in rich edit controls, attempts to change protected text result in an <a href="/windows/desktop/Controls/en-protected">EN_PROTECTED</a> notification code to the creator of the document, who then can refuse or grant permission for the change. The creator is the client that created a windowed rich edit control through the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> function or the <a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a> object that called the <a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function to create a windowless rich edit control.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/Controls/en-protected">EN_PROTECTED</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setprotected">SetProtected</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>