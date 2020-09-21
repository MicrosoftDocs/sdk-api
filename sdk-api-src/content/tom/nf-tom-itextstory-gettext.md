---
UID: NF:tom.ITextStory.GetText
title: ITextStory::GetText (tom.h)
description: Gets the text in a story according to the specified conversion flags.
helpviewer_keywords: ["GetText","GetText method [Windows Controls]","GetText method [Windows Controls]","ITextStory interface","ITextStory interface [Windows Controls]","GetText method","ITextStory.GetText","ITextStory::GetText","controls.itextstory_gettext","tom/ITextStory::GetText","tomAdjustCRLF","tomAllowFinalEOP","tomFoldMathAlpha","tomIncludeNumbering","tomLanguageTag","tomNoHidden","tomNoMathZoneBrackets","tomTextize","tomTranslateTableCell","tomUseCRLF"]
old-location: controls\itextstory_gettext.htm
tech.root: Controls
ms.assetid: 8107910f-eb77-4313-97f5-1bd8126d6dec
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Windows Controls], GetText method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetText method, ITextStory.GetText, ITextStory::GetText, controls.itextstory_gettext, tom/ITextStory::GetText, tomAdjustCRLF, tomAllowFinalEOP, tomFoldMathAlpha, tomIncludeNumbering, tomLanguageTag, tomNoHidden, tomNoMathZoneBrackets, tomTextize, tomTranslateTableCell, tomUseCRLF
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory::GetText
 - tom/ITextStory::GetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetText
---

# ITextStory::GetText


## -description

Gets the text in a story according to the specified conversion flags.

## -parameters

### -param Flags [in]

Type: <b>long</b>

The conversion flags.

A <i>Flags</i> value of 0 retrieves text the same as <a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">ITextRange::GetText</a>.  Other values include the following.

<a id="tomAdjustCRLF"></a>
<a id="tomadjustcrlf"></a>
<a id="TOMADJUSTCRLF"></a>


#### tomAdjustCRLF

<a id="tomAllowFinalEOP"></a>
<a id="tomallowfinaleop"></a>
<a id="TOMALLOWFINALEOP"></a>


#### tomAllowFinalEOP

<a id="tomFoldMathAlpha"></a>
<a id="tomfoldmathalpha"></a>
<a id="TOMFOLDMATHALPHA"></a>


#### tomFoldMathAlpha

<a id="tomIncludeNumbering"></a>
<a id="tomincludenumbering"></a>
<a id="TOMINCLUDENUMBERING"></a>


#### tomIncludeNumbering

<a id="tomNoHidden"></a>
<a id="tomnohidden"></a>
<a id="TOMNOHIDDEN"></a>


#### tomNoHidden

<a id="tomNoMathZoneBrackets"></a>
<a id="tomnomathzonebrackets"></a>
<a id="TOMNOMATHZONEBRACKETS"></a>


#### tomNoMathZoneBrackets

<a id="tomLanguageTag"></a>
<a id="tomlanguagetag"></a>
<a id="TOMLANGUAGETAG"></a>


#### tomLanguageTag

<a id="tomTextize"></a>
<a id="tomtextize"></a>
<a id="TOMTEXTIZE"></a>


#### tomTextize

<a id="tomTranslateTableCell"></a>
<a id="tomtranslatetablecell"></a>
<a id="TOMTRANSLATETABLECELL"></a>


#### tomTranslateTableCell

<a id="tomUseCRLF"></a>
<a id="tomusecrlf"></a>
<a id="TOMUSECRLF"></a>


#### tomUseCRLF

### -param pbstr [out]

Type: <b>BSTR*</b>

The text in the story.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

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

This method is similar to using <a href="/windows/desktop/api/tom/nf-tom-itextrange2-gettext2">ITextRange2::GetText2</a> for a whole story, but it doesn’t require a range.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-settext">ITextStory::SetText</a>