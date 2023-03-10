---
UID: NF:tom.ITextFont.GetLanguageID
title: ITextFont::GetLanguageID (tom.h)
description: Gets the language ID or language code identifier (LCID).
helpviewer_keywords: ["GetLanguageID","GetLanguageID method [Windows Controls]","GetLanguageID method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetLanguageID method","ITextFont.GetLanguageID","ITextFont::GetLanguageID","_win32_ITextFont_GetLanguageID","_win32_ITextFont_GetLanguageID_cpp","controls.ITextFont_GetLanguageID","controls._win32_ITextFont_GetLanguageID","tom/ITextFont::GetLanguageID"]
old-location: controls\ITextFont_GetLanguageID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlanguageid.htm
ms.date: 12/05/2018
ms.keywords: GetLanguageID, GetLanguageID method [Windows Controls], GetLanguageID method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetLanguageID method, ITextFont.GetLanguageID, ITextFont::GetLanguageID, _win32_ITextFont_GetLanguageID, _win32_ITextFont_GetLanguageID_cpp, controls.ITextFont_GetLanguageID, controls._win32_ITextFont_GetLanguageID, tom/ITextFont::GetLanguageID
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
 - ITextFont::GetLanguageID
 - tom/ITextFont::GetLanguageID
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
 - ITextFont.GetLanguageID
---

# ITextFont::GetLanguageID


## -description

Gets the  language ID or language code identifier (LCID).

## -parameters

### -param pValue

Type: <b>long*</b>

The language ID or LCID. The low word contains the language identifier. The high word is either zero or it contains the high word of the LCID. To retrieve the language identifier, mask out the high word. For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.

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

To get the BCP-47 language tag, such as "en-US", call <code>ITextRange2::GetText2(pBstr, tomLanguageTag)</code>, where <i>pBstr</i> specifies the desired language tag.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setlanguageid">SetLanguageID</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>