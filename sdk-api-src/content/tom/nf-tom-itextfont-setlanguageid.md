---
UID: NF:tom.ITextFont.SetLanguageID
title: ITextFont::SetLanguageID (tom.h)
description: Sets the language ID or language code identifier (LCID).
helpviewer_keywords: ["ITextFont interface [Windows Controls]","SetLanguageID method","ITextFont.SetLanguageID","ITextFont::SetLanguageID","SetLanguageID","SetLanguageID method [Windows Controls]","SetLanguageID method [Windows Controls]","ITextFont interface","_win32_ITextFont_SetLanguageID","_win32_ITextFont_SetLanguageID_cpp","controls.ITextFont_SetLanguageID","controls._win32_ITextFont_SetLanguageID","tom/ITextFont::SetLanguageID"]
old-location: controls\ITextFont_SetLanguageID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setlanguageid.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],SetLanguageID method, ITextFont.SetLanguageID, ITextFont::SetLanguageID, SetLanguageID, SetLanguageID method [Windows Controls], SetLanguageID method [Windows Controls],ITextFont interface, _win32_ITextFont_SetLanguageID, _win32_ITextFont_SetLanguageID_cpp, controls.ITextFont_SetLanguageID, controls._win32_ITextFont_SetLanguageID, tom/ITextFont::SetLanguageID
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
 - ITextFont::SetLanguageID
 - tom/ITextFont::SetLanguageID
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
 - ITextFont.SetLanguageID
---

# ITextFont::SetLanguageID


## -description

Sets the  language ID or language code identifier (LCID).

## -parameters

### -param Value [in]

Type: <b>long</b>

The new language identifier. The low word contains the language identifier. The high word is either zero or it contains the high word of the locale identifier LCID. For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.

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

If the high nibble of  <i>Value</i> is <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomCharset</a>, set the <i>charrep</i> from the <i>charset</i> in the low byte and the pitch and family from the next byte. See also <a href="/windows/desktop/api/tom/nf-tom-itextfont2-setcharrep">ITextFont2::SetCharRep</a>. 

If the high nibble of <i>Value</i> is <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomCharRepFromLcid</a>, set the <i>charrep</i> from the LCID and set the LCID as well. See <a href="/windows/desktop/api/tom/nf-tom-itextfont-getlanguageid">ITextFont::GetLanguageID</a> for more information. 


To set the BCP-47 language tag, such as "en-US", call <a href="/windows/desktop/api/tom/nf-tom-itextrange2-settext2">ITextRange2::SetText2</a> and set the <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomLanguageTag</a> and <i>bstr</i> with the language tag.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-getlanguageid">GetLanguageID</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>