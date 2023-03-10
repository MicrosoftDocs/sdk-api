---
UID: NF:msime.IFEDictionary.GetWords
title: IFEDictionary::GetWords (msime.h)
description: Gets word entries from a dictionary.
helpviewer_keywords: ["GetWords","GetWords method [Internationalization for Windows Applications]","GetWords method [Internationalization for Windows Applications]","IFEDictionary interface","IFED_POS_ADJECTIVE","IFED_POS_ADJECTIVE_VERB","IFED_POS_ADNOUN","IFED_POS_ADVERB","IFED_POS_AFFIX","IFED_POS_ALL","IFED_POS_AUXILIARY_VERB","IFED_POS_CONJUNCTION","IFED_POS_DEPENDENT","IFED_POS_IDIOMS","IFED_POS_INDEPENDENT","IFED_POS_INFLECTIONALSUFFIX","IFED_POS_INTERJECTION","IFED_POS_NONE","IFED_POS_NOUN","IFED_POS_PARTICLE","IFED_POS_PREFIX","IFED_POS_SUB_VERB","IFED_POS_SUFFIX","IFED_POS_SYMBOLS","IFED_POS_TANKANJI","IFED_POS_VERB","IFED_REG_ALL","IFED_REG_AUTO","IFED_REG_GRAMMAR","IFED_REG_NONE","IFED_REG_USER","IFED_SELECT_ALL","IFED_SELECT_COMMENT","IFED_SELECT_DISPLAY","IFED_SELECT_NONE","IFED_SELECT_POS","IFED_SELECT_READING","IFEDictionary interface [Internationalization for Windows Applications]","GetWords method","IFEDictionary.GetWords","IFEDictionary::GetWords","NULL","intl.ifedictionary_getwords","msime/IFEDictionary::GetWords"]
old-location: intl\ifedictionary_getwords.htm
tech.root: Intl
ms.assetid: 9FEA7E1C-166B-4CA4-B25E-0406AD60AC0B
ms.date: 12/05/2018
ms.keywords: GetWords, GetWords method [Internationalization for Windows Applications], GetWords method [Internationalization for Windows Applications],IFEDictionary interface, IFED_POS_ADJECTIVE, IFED_POS_ADJECTIVE_VERB, IFED_POS_ADNOUN, IFED_POS_ADVERB, IFED_POS_AFFIX, IFED_POS_ALL, IFED_POS_AUXILIARY_VERB, IFED_POS_CONJUNCTION, IFED_POS_DEPENDENT, IFED_POS_IDIOMS, IFED_POS_INDEPENDENT, IFED_POS_INFLECTIONALSUFFIX, IFED_POS_INTERJECTION, IFED_POS_NONE, IFED_POS_NOUN, IFED_POS_PARTICLE, IFED_POS_PREFIX, IFED_POS_SUB_VERB, IFED_POS_SUFFIX, IFED_POS_SYMBOLS, IFED_POS_TANKANJI, IFED_POS_VERB, IFED_REG_ALL, IFED_REG_AUTO, IFED_REG_GRAMMAR, IFED_REG_NONE, IFED_REG_USER, IFED_SELECT_ALL, IFED_SELECT_COMMENT, IFED_SELECT_DISPLAY, IFED_SELECT_NONE, IFED_SELECT_POS, IFED_SELECT_READING, IFEDictionary interface [Internationalization for Windows Applications],GetWords method, IFEDictionary.GetWords, IFEDictionary::GetWords, NULL, intl.ifedictionary_getwords, msime/IFEDictionary::GetWords
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
 - IFEDictionary::GetWords
 - msime/IFEDictionary::GetWords
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
 - IFEDictionary.GetWords
---

# IFEDictionary::GetWords


## -description

Gets word entries from a dictionary.

The selection of a word entry can be performed by a combination of<ul>
<li>A string with Japanese phonetic characters, with or without a wildcard at the end of the string.</li>
<li>A word, with or without a wildcard at its end.</li>
<li>A Part of Speech</li>
</ul>In addition, retrievals by a string with Japanese phonetic characters can be performed by specifying a range in the Hiragana 50-on ordering.

## -parameters

### -param pwchFirst [in]

A text string against which <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> entries are matched; the value must be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Low-value.

</td>
</tr>
<tr>
<td width="40%"></td>
<td width="60%">
Hiragana string (full text to be retrieved).

</td>
</tr>
<tr>
<td width="40%"></td>
<td width="60%">
Hiragana string ending in "*" (specifying only leading characters of text).

This can be an initial text string when a range of words is to be retrieved, in which case a wildcard must not be used.

</td>
</tr>
</table>

### -param pwchLast [in]

A text string that is used to end a text string. This must contain the same value as <b>pwchReading</b> in the <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structure when a retrieval is performed by a single value; that is, not by a range value. The value must be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
High-value.

</td>
</tr>
<tr>
<td width="40%"></td>
<td width="60%">
Hiragana string (full text to be retrieved).

</td>
</tr>
<tr>
<td width="40%"></td>
<td width="60%">
Hiragana string ending in "*" (specifying only leading characters of text).

</td>
</tr>
</table>

### -param pwchDisplay [in]

A display string against which <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> entries are matched; the value must be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Means "*".

</td>
</tr>
<tr>
<td width="40%"></td>
<td width="60%">
Any Japanese string.

</td>
</tr>
<tr>
<td width="40%"></td>
<td width="60%">
Japanese string ending in "*".

</td>
</tr>
</table>

### -param ulPos [in]

Filter(s) on the Microsoft IME public Parts of Speech. This is a combination of one or more of the following flags:

<a id="IFED_POS_NONE"></a>
<a id="ifed_pos_none"></a>


#### IFED_POS_NONE

<a id="IFED_POS_NOUN"></a>
<a id="ifed_pos_noun"></a>


#### IFED_POS_NOUN

<a id="IFED_POS_VERB"></a>
<a id="ifed_pos_verb"></a>


#### IFED_POS_VERB

<a id="IFED_POS_ADJECTIVE"></a>
<a id="ifed_pos_adjective"></a>


#### IFED_POS_ADJECTIVE

<a id="IFED_POS_ADJECTIVE_VERB"></a>
<a id="ifed_pos_adjective_verb"></a>


#### IFED_POS_ADJECTIVE_VERB

<a id="IFED_POS_ADVERB"></a>
<a id="ifed_pos_adverb"></a>


#### IFED_POS_ADVERB

<a id="IFED_POS_ADNOUN"></a>
<a id="ifed_pos_adnoun"></a>


#### IFED_POS_ADNOUN

<a id="IFED_POS_CONJUNCTION"></a>
<a id="ifed_pos_conjunction"></a>


#### IFED_POS_CONJUNCTION

<a id="IFED_POS_INTERJECTION"></a>
<a id="ifed_pos_interjection"></a>


#### IFED_POS_INTERJECTION

<a id="IFED_POS_INDEPENDENT"></a>
<a id="ifed_pos_independent"></a>


#### IFED_POS_INDEPENDENT

<a id="IFED_POS_INFLECTIONALSUFFIX"></a>
<a id="ifed_pos_inflectionalsuffix"></a>


#### IFED_POS_INFLECTIONALSUFFIX

<a id="IFED_POS_PREFIX"></a>
<a id="ifed_pos_prefix"></a>


#### IFED_POS_PREFIX

<a id="IFED_POS_SUFFIX"></a>
<a id="ifed_pos_suffix"></a>


#### IFED_POS_SUFFIX

<a id="IFED_POS_AFFIX"></a>
<a id="ifed_pos_affix"></a>


#### IFED_POS_AFFIX

<a id="IFED_POS_TANKANJI"></a>
<a id="ifed_pos_tankanji"></a>


#### IFED_POS_TANKANJI

<a id="IFED_POS_IDIOMS"></a>
<a id="ifed_pos_idioms"></a>


#### IFED_POS_IDIOMS

<a id="IFED_POS_SYMBOLS"></a>
<a id="ifed_pos_symbols"></a>


#### IFED_POS_SYMBOLS

<a id="IFED_POS_PARTICLE"></a>
<a id="ifed_pos_particle"></a>


#### IFED_POS_PARTICLE

<a id="IFED_POS_AUXILIARY_VERB"></a>
<a id="ifed_pos_auxiliary_verb"></a>


#### IFED_POS_AUXILIARY_VERB

<a id="IFED_POS_SUB_VERB"></a>
<a id="ifed_pos_sub_verb"></a>


#### IFED_POS_SUB_VERB

<a id="IFED_POS_DEPENDENT"></a>
<a id="ifed_pos_dependent"></a>


#### IFED_POS_DEPENDENT

<a id="IFED_POS_ALL"></a>
<a id="ifed_pos_all"></a>


#### IFED_POS_ALL

### -param ulSelect [in]

Specifies the query output of a word. This is a combination of one or more of the following flags:

<a id="IFED_SELECT_NONE"></a>
<a id="ifed_select_none"></a>


#### IFED_SELECT_NONE

<a id="IFED_SELECT_READING"></a>
<a id="ifed_select_reading"></a>


#### IFED_SELECT_READING

<a id="IFED_SELECT_DISPLAY"></a>
<a id="ifed_select_display"></a>


#### IFED_SELECT_DISPLAY

<a id="IFED_SELECT_POS"></a>
<a id="ifed_select_pos"></a>


#### IFED_SELECT_POS

<a id="IFED_SELECT_COMMENT"></a>
<a id="ifed_select_comment"></a>


#### IFED_SELECT_COMMENT

<a id="IFED_SELECT_ALL"></a>
<a id="ifed_select_all"></a>


#### IFED_SELECT_ALL

### -param ulWordSrc [in]

Specifies the word source. When the <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> is a user dictionary, this is a combination of one or more of the following flags:

<a id="IFED_REG_NONE"></a>
<a id="ifed_reg_none"></a>


#### IFED_REG_NONE

<a id="IFED_REG_USER"></a>
<a id="ifed_reg_user"></a>


#### IFED_REG_USER

<a id="IFED_REG_AUTO"></a>
<a id="ifed_reg_auto"></a>


#### IFED_REG_AUTO

<a id="IFED_REG_GRAMMAR"></a>
<a id="ifed_reg_grammar"></a>


#### IFED_REG_GRAMMAR

<a id="IFED_REG_ALL"></a>
<a id="ifed_reg_all"></a>


#### IFED_REG_ALL

### -param pchBuffer [in, out]

Buffer provided by the caller to receive the data.

### -param cbBuffer [in]

The size of <i>pchBuffer</i>.

### -param pcWrd [out]

The number of <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structures returned in <i>pchBuffer</i>. If more entries are found than <i>pchBuffer</i> can store, <b>IFED_S_MORE_ENTRIES</b> will be returned.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_S_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
The client must call <a href="/windows/desktop/api/msime/nf-msime-ifedictionary-nextwords">NextWords</a> to get additional <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_E_NO_ENTRY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-nextwords">NextWords</a>