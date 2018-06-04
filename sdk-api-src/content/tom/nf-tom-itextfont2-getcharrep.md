---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITextFont2::GetCharRep


## -description


Gets the character repertoire (writing system).


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The character repertoire. It can be one of the following values.


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

<a id="tomVietnamese"></a>
<a id="tomvietnamese"></a>
<a id="TOMVIETNAMESE"></a>


#### tomVietnamese

<a id="tomUsymbol"></a>
<a id="tomusymbol"></a>
<a id="TOMUSYMBOL"></a>


#### tomUsymbol

<a id="tomYi"></a>
<a id="tomyi"></a>
<a id="TOMYI"></a>


#### tomYi


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/6c57b5e5-a5c7-416a-851c-fc8ef16b5a9a">ITextFont2::SetCharRep</a>
 

 

