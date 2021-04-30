---
UID: NF:tom.ITextDocument2.GetPreferredFont
title: ITextDocument2::GetPreferredFont (tom.h)
description: Retrieves the preferred font for a particular character repertoire and character position.
helpviewer_keywords: ["GetPreferredFont","GetPreferredFont method [Windows Controls]","GetPreferredFont method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetPreferredFont method","ITextDocument2.GetPreferredFont","ITextDocument2::GetPreferredFont","controls.itextdocument2_getpreferredfont","tom/ITextDocument2::GetPreferredFont","tomAboriginal","tomAnsi","tomArabic","tomArmenian","tomBIG5","tomBaltic","tomBengali","tomBraille","tomCherokee","tomCyrillic","tomDefaultCharRep","tomDevanagari","tomEastEurope","tomEmoji","tomEthiopic","tomGB2312","tomGeorgian","tomGetHeightOnly","tomGreek","tomGujarati","tomGurmukhi","tomHangul","tomHebrew","tomIgnoreCurrentFont","tomJamo","tomKannada","tomKayahli","tomKharoshthi","tomKhmer","tomLao","tomLimbu","tomMac","tomMalayalam","tomMatchAscii","tomMatchCharRep","tomMatchFontSignature","tomMatchMathFont","tomMongolian","tomMyanmar","tomNewTaiLu","tomOEM","tomOgham","tomOriya","tomPC437","tomRunic","tomShiftJIS","tomSinhala","tomSylotinagr","tomSymbol","tomSyriac","tomTaiLe","tomTamil","tomTelugu","tomThaana","tomThai","tomTibetan","tomTurkish","tomUsymbol","tomVietnamese","tomYi"]
old-location: controls\itextdocument2_getpreferredfont.htm
tech.root: Controls
ms.assetid: d07c3093-8050-4c62-8e90-3b09cdb10700
ms.date: 12/05/2018
ms.keywords: GetPreferredFont, GetPreferredFont method [Windows Controls], GetPreferredFont method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetPreferredFont method, ITextDocument2.GetPreferredFont, ITextDocument2::GetPreferredFont, controls.itextdocument2_getpreferredfont, tom/ITextDocument2::GetPreferredFont, tomAboriginal, tomAnsi, tomArabic, tomArmenian, tomBIG5, tomBaltic, tomBengali, tomBraille, tomCherokee, tomCyrillic, tomDefaultCharRep, tomDevanagari, tomEastEurope, tomEmoji, tomEthiopic, tomGB2312, tomGeorgian, tomGetHeightOnly, tomGreek, tomGujarati, tomGurmukhi, tomHangul, tomHebrew, tomIgnoreCurrentFont, tomJamo, tomKannada, tomKayahli, tomKharoshthi, tomKhmer, tomLao, tomLimbu, tomMac, tomMalayalam, tomMatchAscii, tomMatchCharRep, tomMatchFontSignature, tomMatchMathFont, tomMongolian, tomMyanmar, tomNewTaiLu, tomOEM, tomOgham, tomOriya, tomPC437, tomRunic, tomShiftJIS, tomSinhala, tomSylotinagr, tomSymbol, tomSyriac, tomTaiLe, tomTamil, tomTelugu, tomThaana, tomThai, tomTibetan, tomTurkish, tomUsymbol, tomVietnamese, tomYi
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
 - ITextDocument2::GetPreferredFont
 - tom/ITextDocument2::GetPreferredFont
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
 - ITextDocument2.GetPreferredFont
---

# ITextDocument2::GetPreferredFont


## -description

Retrieves the preferred font for a particular character repertoire and character position.

## -parameters

### -param cp [in]

Type: <b>long</b>

The character position for the preferred font.

### -param CharRep [in]

Type: <b>long</b>

The character repertoire index for the preferred font. It can be one of the following values.

<a id="tomAboriginal"></a>
<a id="tomaboriginal"></a>
<a id="TOMABORIGINAL"></a>


#### tomAboriginal

<a id="tomAnsi"></a>
<a id="tomansi"></a>
<a id="TOMANSI"></a>


#### tomAnsi

<a id="tomArabic"></a>
<a id="tomarabic"></a>
<a id="TOMARABIC"></a>


#### tomArabic

<a id="tomArmenian"></a>
<a id="tomarmenian"></a>
<a id="TOMARMENIAN"></a>


#### tomArmenian

<a id="tomBaltic"></a>
<a id="tombaltic"></a>
<a id="TOMBALTIC"></a>


#### tomBaltic

<a id="tomBengali"></a>
<a id="tombengali"></a>
<a id="TOMBENGALI"></a>


#### tomBengali

<a id="tomBIG5"></a>
<a id="tombig5"></a>
<a id="TOMBIG5"></a>


#### tomBIG5

<a id="tomBraille"></a>
<a id="tombraille"></a>
<a id="TOMBRAILLE"></a>


#### tomBraille

<a id="tomCherokee"></a>
<a id="tomcherokee"></a>
<a id="TOMCHEROKEE"></a>


#### tomCherokee

<a id="tomCyrillic"></a>
<a id="tomcyrillic"></a>
<a id="TOMCYRILLIC"></a>


#### tomCyrillic

<a id="tomDefaultCharRep"></a>
<a id="tomdefaultcharrep"></a>
<a id="TOMDEFAULTCHARREP"></a>


#### tomDefaultCharRep

<a id="tomDevanagari"></a>
<a id="tomdevanagari"></a>
<a id="TOMDEVANAGARI"></a>


#### tomDevanagari

<a id="tomEastEurope"></a>
<a id="tomeasteurope"></a>
<a id="TOMEASTEUROPE"></a>


#### tomEastEurope

<a id="tomEmoji"></a>
<a id="tomemoji"></a>
<a id="TOMEMOJI"></a>


#### tomEmoji

<a id="tomEthiopic"></a>
<a id="tomethiopic"></a>
<a id="TOMETHIOPIC"></a>


#### tomEthiopic

<a id="tomGB2312"></a>
<a id="tomgb2312"></a>
<a id="TOMGB2312"></a>


#### tomGB2312

<a id="tomGeorgian"></a>
<a id="tomgeorgian"></a>
<a id="TOMGEORGIAN"></a>


#### tomGeorgian

<a id="tomGreek"></a>
<a id="tomgreek"></a>
<a id="TOMGREEK"></a>


#### tomGreek

<a id="tomGujarati"></a>
<a id="tomgujarati"></a>
<a id="TOMGUJARATI"></a>


#### tomGujarati

<a id="tomGurmukhi"></a>
<a id="tomgurmukhi"></a>
<a id="TOMGURMUKHI"></a>


#### tomGurmukhi

<a id="tomHangul"></a>
<a id="tomhangul"></a>
<a id="TOMHANGUL"></a>


#### tomHangul

<a id="tomHebrew"></a>
<a id="tomhebrew"></a>
<a id="TOMHEBREW"></a>


#### tomHebrew

<a id="tomJamo"></a>
<a id="tomjamo"></a>
<a id="TOMJAMO"></a>


#### tomJamo

<a id="tomKannada"></a>
<a id="tomkannada"></a>
<a id="TOMKANNADA"></a>


#### tomKannada

<a id="tomKayahli"></a>
<a id="tomkayahli"></a>
<a id="TOMKAYAHLI"></a>


#### tomKayahli

<a id="tomKharoshthi"></a>
<a id="tomkharoshthi"></a>
<a id="TOMKHAROSHTHI"></a>


#### tomKharoshthi

<a id="tomKhmer"></a>
<a id="tomkhmer"></a>
<a id="TOMKHMER"></a>


#### tomKhmer

<a id="tomLao"></a>
<a id="tomlao"></a>
<a id="TOMLAO"></a>


#### tomLao

<a id="tomLimbu"></a>
<a id="tomlimbu"></a>
<a id="TOMLIMBU"></a>


#### tomLimbu

<a id="tomMac"></a>
<a id="tommac"></a>
<a id="TOMMAC"></a>


#### tomMac

<a id="tomMalayalam"></a>
<a id="tommalayalam"></a>
<a id="TOMMALAYALAM"></a>


#### tomMalayalam

<a id="tomMongolian"></a>
<a id="tommongolian"></a>
<a id="TOMMONGOLIAN"></a>


#### tomMongolian

<a id="tomMyanmar"></a>
<a id="tommyanmar"></a>
<a id="TOMMYANMAR"></a>


#### tomMyanmar

<a id="tomNewTaiLu"></a>
<a id="tomnewtailu"></a>
<a id="TOMNEWTAILU"></a>


#### tomNewTaiLu

<a id="tomOEM"></a>
<a id="tomoem"></a>
<a id="TOMOEM"></a>


#### tomOEM

<a id="tomOgham"></a>
<a id="tomogham"></a>
<a id="TOMOGHAM"></a>


#### tomOgham

<a id="tomOriya"></a>
<a id="tomoriya"></a>
<a id="TOMORIYA"></a>


#### tomOriya

<a id="tomPC437"></a>
<a id="tompc437"></a>
<a id="TOMPC437"></a>


#### tomPC437

<a id="tomRunic"></a>
<a id="tomrunic"></a>
<a id="TOMRUNIC"></a>


#### tomRunic

<a id="tomShiftJIS"></a>
<a id="tomshiftjis"></a>
<a id="TOMSHIFTJIS"></a>


#### tomShiftJIS

<a id="tomSinhala"></a>
<a id="tomsinhala"></a>
<a id="TOMSINHALA"></a>


#### tomSinhala

<a id="tomSylotinagr"></a>
<a id="tomsylotinagr"></a>
<a id="TOMSYLOTINAGR"></a>


#### tomSylotinagr

<a id="tomSymbol"></a>
<a id="tomsymbol"></a>
<a id="TOMSYMBOL"></a>


#### tomSymbol

<a id="tomSyriac"></a>
<a id="tomsyriac"></a>
<a id="TOMSYRIAC"></a>


#### tomSyriac

<a id="tomTaiLe"></a>
<a id="tomtaile"></a>
<a id="TOMTAILE"></a>


#### tomTaiLe

<a id="tomTamil"></a>
<a id="tomtamil"></a>
<a id="TOMTAMIL"></a>


#### tomTamil

<a id="tomTelugu"></a>
<a id="tomtelugu"></a>
<a id="TOMTELUGU"></a>


#### tomTelugu

<a id="tomThaana"></a>
<a id="tomthaana"></a>
<a id="TOMTHAANA"></a>


#### tomThaana

<a id="tomThai"></a>
<a id="tomthai"></a>
<a id="TOMTHAI"></a>


#### tomThai

<a id="tomTibetan"></a>
<a id="tomtibetan"></a>
<a id="TOMTIBETAN"></a>


#### tomTibetan

<a id="tomTurkish"></a>
<a id="tomturkish"></a>
<a id="TOMTURKISH"></a>


#### tomTurkish

<a id="tomUsymbol"></a>
<a id="tomusymbol"></a>
<a id="TOMUSYMBOL"></a>


#### tomUsymbol

<a id="tomVietnamese"></a>
<a id="tomvietnamese"></a>
<a id="TOMVIETNAMESE"></a>


#### tomVietnamese

<a id="tomYi"></a>
<a id="tomyi"></a>
<a id="TOMYI"></a>


#### tomYi

### -param Options [in]

Type: <b>long</b>

The preferred font options. The low-order word can be a combination of the following values. 

<a id="tomIgnoreCurrentFont"></a>
<a id="tomignorecurrentfont"></a>
<a id="TOMIGNORECURRENTFONT"></a>


#### tomIgnoreCurrentFont

<a id="tomMatchCharRep"></a>
<a id="tommatchcharrep"></a>
<a id="TOMMATCHCHARREP"></a>


#### tomMatchCharRep

<a id="tomMatchFontSignature"></a>
<a id="tommatchfontsignature"></a>
<a id="TOMMATCHFONTSIGNATURE"></a>


#### tomMatchFontSignature

<a id="tomMatchAscii"></a>
<a id="tommatchascii"></a>
<a id="TOMMATCHASCII"></a>


#### tomMatchAscii

<a id="tomGetHeightOnly"></a>
<a id="tomgetheightonly"></a>
<a id="TOMGETHEIGHTONLY"></a>


#### tomGetHeightOnly

<a id="tomMatchMathFont"></a>
<a id="tommatchmathfont"></a>
<a id="TOMMATCHMATHFONT"></a>


#### tomMatchMathFont

If the high-order word of <i>Options</i> is <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUseTwips</a>, the font heights are given in twips.

### -param curCharRep [in]

Type: <b>long</b>

The index of the current character repertoire.

### -param curFontSize [in]

Type: <b>long</b>

The current font size.

### -param pbstr [out]

Type: <b>BSTR*</b>

The name of the font.

### -param pPitchAndFamily [out]

Type: <b>long*</b>

The font pitch and family.

### -param pNewFontSize [out]

Type: <b>long*</b>

The new font size.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>