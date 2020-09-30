---
UID: NF:tom.ITextRange2.GetText2
title: ITextRange2::GetText2 (tom.h)
description: Gets the text in this range according to the specified conversion flags.
helpviewer_keywords: ["GetText2","GetText2 method [Windows Controls]","GetText2 method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetText2 method","ITextRange2.GetText2","ITextRange2::GetText2","controls.itextrange2_gettext2","tom/ITextRange2::GetText2","tomAdjustCRLF","tomAllowFinalEOP","tomFoldMathAlpha","tomIncludeNumbering","tomLanguageTag","tomNoHidden","tomNoMathZoneBrackets","tomTextize","tomTranslateTableCell","tomUseCRLF"]
old-location: controls\itextrange2_gettext2.htm
tech.root: Controls
ms.assetid: 77f39808-b39d-45bb-ba03-3a27d503fe0e
ms.date: 12/05/2018
ms.keywords: GetText2, GetText2 method [Windows Controls], GetText2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetText2 method, ITextRange2.GetText2, ITextRange2::GetText2, controls.itextrange2_gettext2, tom/ITextRange2::GetText2, tomAdjustCRLF, tomAllowFinalEOP, tomFoldMathAlpha, tomIncludeNumbering, tomLanguageTag, tomNoHidden, tomNoMathZoneBrackets, tomTextize, tomTranslateTableCell, tomUseCRLF
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
 - ITextRange2::GetText2
 - tom/ITextRange2::GetText2
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
 - ITextRange2.GetText2
---

# ITextRange2::GetText2


## -description

Gets the text in this range according to the specified conversion flags.

## -parameters

### -param Flags [in]

Type: <b>long</b>

The flags controlling how the text is retrieved. The flags can include a combination of the following values. Specifying a <i>Flags</i> value of 0 is the same as calling the  <a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">ITextRange::GetText</a> method.  

<a id="tomAdjustCRLF"></a>
<a id="tomadjustcrlf"></a>
<a id="TOMADJUSTCRLF"></a>


#### tomAdjustCRLF

<a id="tomUseCRLF"></a>
<a id="tomusecrlf"></a>
<a id="TOMUSECRLF"></a>


#### tomUseCRLF

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

<a id="tomTextize"></a>
<a id="tomtextize"></a>
<a id="TOMTEXTIZE"></a>


#### tomTextize

<a id="tomAllowFinalEOP"></a>
<a id="tomallowfinaleop"></a>
<a id="TOMALLOWFINALEOP"></a>


#### tomAllowFinalEOP

<a id="tomTranslateTableCell"></a>
<a id="tomtranslatetablecell"></a>
<a id="TOMTRANSLATETABLECELL"></a>


#### tomTranslateTableCell

<a id="tomFoldMathAlpha"></a>
<a id="tomfoldmathalpha"></a>
<a id="TOMFOLDMATHALPHA"></a>


#### tomFoldMathAlpha

<a id="tomLanguageTag"></a>
<a id="tomlanguagetag"></a>
<a id="TOMLANGUAGETAG"></a>


#### tomLanguageTag

### -param pbstr [out]

Type: <b>BSTR*</b>

The text in the range.

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

This method includes the special flag <b>tomLanguageTag</b> to get the BCP-47 language tag for the range. This is an industry standard language tag which may be preferable to the language code identifier (LCID) obtained by calling <a href="/windows/desktop/api/tom/nf-tom-itextfont-getlanguageid">ITextFont::GetLanguageID</a>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-settext2">ITextRange2::SetText2</a>