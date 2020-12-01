---
UID: NF:msime.IFELanguage.GetConversionModeCaps
title: IFELanguage::GetConversionModeCaps (msime.h)
description: Gets the conversion mode capability of the IFELanguage object.
helpviewer_keywords: ["FELANG_CMODE_AUTOMATIC","FELANG_CMODE_BESTFIRST","FELANG_CMODE_BOPOMOFO","FELANG_CMODE_CONVERSATION","FELANG_CMODE_FULLWIDTHOUT","FELANG_CMODE_HALFWIDTHOUT","FELANG_CMODE_HANGUL","FELANG_CMODE_HIRAGANAOUT","FELANG_CMODE_KATAKANAOUT","FELANG_CMODE_MERGECAND","FELANG_CMODE_MONORUBY","FELANG_CMODE_NAME","FELANG_CMODE_NOINVISIBLECHAR","FELANG_CMODE_NONE","FELANG_CMODE_NOPRUNING","FELANG_CMODE_PHRASEPREDICT","FELANG_CMODE_PINYIN","FELANG_CMODE_PLAURALCLAUSE","FELANG_CMODE_PRECONV","FELANG_CMODE_RADICAL","FELANG_CMODE_ROMAN","FELANG_CMODE_SINGLECONVERT","FELANG_CMODE_UNKNOWNREADING","FELANG_CMODE_USENOREVWORDS","GetConversionModeCaps","GetConversionModeCaps method [Internationalization for Windows Applications]","GetConversionModeCaps method [Internationalization for Windows Applications]","IFELanguage interface","IFELanguage interface [Internationalization for Windows Applications]","GetConversionModeCaps method","IFELanguage.GetConversionModeCaps","IFELanguage::GetConversionModeCaps","intl.ifelanguage_getconversionmodecaps","msime/IFELanguage::GetConversionModeCaps"]
old-location: intl\ifelanguage_getconversionmodecaps.htm
tech.root: Intl
ms.assetid: B1A3D121-C650-4D04-9278-791A12F73A2E
ms.date: 12/05/2018
ms.keywords: FELANG_CMODE_AUTOMATIC, FELANG_CMODE_BESTFIRST, FELANG_CMODE_BOPOMOFO, FELANG_CMODE_CONVERSATION, FELANG_CMODE_FULLWIDTHOUT, FELANG_CMODE_HALFWIDTHOUT, FELANG_CMODE_HANGUL, FELANG_CMODE_HIRAGANAOUT, FELANG_CMODE_KATAKANAOUT, FELANG_CMODE_MERGECAND, FELANG_CMODE_MONORUBY, FELANG_CMODE_NAME, FELANG_CMODE_NOINVISIBLECHAR, FELANG_CMODE_NONE, FELANG_CMODE_NOPRUNING, FELANG_CMODE_PHRASEPREDICT, FELANG_CMODE_PINYIN, FELANG_CMODE_PLAURALCLAUSE, FELANG_CMODE_PRECONV, FELANG_CMODE_RADICAL, FELANG_CMODE_ROMAN, FELANG_CMODE_SINGLECONVERT, FELANG_CMODE_UNKNOWNREADING, FELANG_CMODE_USENOREVWORDS, GetConversionModeCaps, GetConversionModeCaps method [Internationalization for Windows Applications], GetConversionModeCaps method [Internationalization for Windows Applications],IFELanguage interface, IFELanguage interface [Internationalization for Windows Applications],GetConversionModeCaps method, IFELanguage.GetConversionModeCaps, IFELanguage::GetConversionModeCaps, intl.ifelanguage_getconversionmodecaps, msime/IFELanguage::GetConversionModeCaps
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFELanguage::GetConversionModeCaps
 - msime/IFELanguage::GetConversionModeCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFELanguage.GetConversionModeCaps
---

# IFELanguage::GetConversionModeCaps


## -description

Gets the conversion mode capability of the <a href="/windows/desktop/api/msime/nn-msime-ifelanguage">IFELanguage</a> object.

## -parameters

### -param pdwCaps [out]

The capabilities, represented as a combination of one or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_MONORUBY"></a><a id="felang_cmode_monoruby"></a><dl>
<dt><b>FELANG_CMODE_MONORUBY</b></dt>
</dl>
</td>
<td width="60%">
Mono-ruby.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_NOPRUNING"></a><a id="felang_cmode_nopruning"></a><dl>
<dt><b>FELANG_CMODE_NOPRUNING</b></dt>
</dl>
</td>
<td width="60%">
No pruning.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_KATAKANAOUT"></a><a id="felang_cmode_katakanaout"></a><dl>
<dt><b>FELANG_CMODE_KATAKANAOUT</b></dt>
</dl>
</td>
<td width="60%">
Katakana output.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_HIRAGANAOUT"></a><a id="felang_cmode_hiraganaout"></a><dl>
<dt><b>FELANG_CMODE_HIRAGANAOUT</b></dt>
</dl>
</td>
<td width="60%">
Default output.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_HALFWIDTHOUT"></a><a id="felang_cmode_halfwidthout"></a><dl>
<dt><b>FELANG_CMODE_HALFWIDTHOUT</b></dt>
</dl>
</td>
<td width="60%">
Half-width output.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_FULLWIDTHOUT"></a><a id="felang_cmode_fullwidthout"></a><dl>
<dt><b>FELANG_CMODE_FULLWIDTHOUT</b></dt>
</dl>
</td>
<td width="60%">
Full-width output.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_BOPOMOFO"></a><a id="felang_cmode_bopomofo"></a><dl>
<dt><b>FELANG_CMODE_BOPOMOFO</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_HANGUL"></a><a id="felang_cmode_hangul"></a><dl>
<dt><b>FELANG_CMODE_HANGUL</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_PINYIN"></a><a id="felang_cmode_pinyin"></a><dl>
<dt><b>FELANG_CMODE_PINYIN</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_PRECONV"></a><a id="felang_cmode_preconv"></a><dl>
<dt><b>FELANG_CMODE_PRECONV</b></dt>
</dl>
</td>
<td width="60%">
Do conversion as follows:

<ul>
<li>Roma-ji to kana.</li>
<li>Autocorrect before conversion.</li>
<li>Periods, comma, and brackets.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_RADICAL"></a><a id="felang_cmode_radical"></a><dl>
<dt><b>FELANG_CMODE_RADICAL</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_UNKNOWNREADING"></a><a id="felang_cmode_unknownreading"></a><dl>
<dt><b>FELANG_CMODE_UNKNOWNREADING</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_MERGECAND"></a><a id="felang_cmode_mergecand"></a><dl>
<dt><b>FELANG_CMODE_MERGECAND</b></dt>
</dl>
</td>
<td width="60%">
Merge display with the same candidate.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_ROMAN"></a><a id="felang_cmode_roman"></a><dl>
<dt><b>FELANG_CMODE_ROMAN</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_BESTFIRST"></a><a id="felang_cmode_bestfirst"></a><dl>
<dt><b>FELANG_CMODE_BESTFIRST</b></dt>
</dl>
</td>
<td width="60%">
Make only the first best.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_USENOREVWORDS"></a><a id="felang_cmode_usenorevwords"></a><dl>
<dt><b>FELANG_CMODE_USENOREVWORDS</b></dt>
</dl>
</td>
<td width="60%">
Use invalid revword on REV/RECONV.

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_NONE"></a><a id="felang_cmode_none"></a><dl>
<dt><b>FELANG_CMODE_NONE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Intl/ime-sentence-mode-values">IME_SMODE_NONE</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_PLAURALCLAUSE"></a><a id="felang_cmode_plauralclause"></a><dl>
<dt><b>FELANG_CMODE_PLAURALCLAUSE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Intl/ime-sentence-mode-values">IME_SMODE_PLAURALCLAUSE</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_SINGLECONVERT"></a><a id="felang_cmode_singleconvert"></a><dl>
<dt><b>FELANG_CMODE_SINGLECONVERT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Intl/ime-sentence-mode-values">IME_SMODE_SINGLECONVERT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_AUTOMATIC"></a><a id="felang_cmode_automatic"></a><dl>
<dt><b>FELANG_CMODE_AUTOMATIC</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Intl/ime-sentence-mode-values">IME_SMODE_AUTOMATIC</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_PHRASEPREDICT"></a><a id="felang_cmode_phrasepredict"></a><dl>
<dt><b>FELANG_CMODE_PHRASEPREDICT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Intl/ime-sentence-mode-values">IME_SMODE_PHRASEPREDICT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_CONVERSATION"></a><a id="felang_cmode_conversation"></a><dl>
<dt><b>FELANG_CMODE_CONVERSATION</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Intl/ime-sentence-mode-values">IME_SMODE_CONVERSATION</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_NAME"></a><a id="felang_cmode_name"></a><dl>
<dt><b>FELANG_CMODE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Name mode (MSKKIME).

</td>
</tr>
<tr>
<td width="40%"><a id="FELANG_CMODE_NOINVISIBLECHAR"></a><a id="felang_cmode_noinvisiblechar"></a><dl>
<dt><b>FELANG_CMODE_NOINVISIBLECHAR</b></dt>
</dl>
</td>
<td width="60%">
Remove invisible chars (for example, the tone mark).

</td>
</tr>
</table>

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifelanguage">IFELanguage</a>