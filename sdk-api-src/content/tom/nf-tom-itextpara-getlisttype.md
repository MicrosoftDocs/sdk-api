---
UID: NF:tom.ITextPara.GetListType
title: ITextPara::GetListType (tom.h)
description: Retrieves the kind of numbering to use with paragraphs.
helpviewer_keywords: ["GetListType","GetListType method [Windows Controls]","GetListType method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetListType method","ITextPara.GetListType","ITextPara::GetListType","_win32_ITextPara_GetListType","_win32_ITextPara_GetListType_cpp","controls.ITextPara_GetListType","controls._win32_ITextPara_GetListType","tom/ITextPara::GetListType","tomListBullet","tomListMinus","tomListNone","tomListNumberAsArabic","tomListNumberAsLCLetter","tomListNumberAsLCRoman","tomListNumberAsSequence","tomListNumberAsUCLetter","tomListNumberAsUCRoman","tomListNumberedArabic1","tomListNumberedArabic2","tomListNumberedArabicWide","tomListNumberedBlackCircleWingding","tomListNumberedChS","tomListNumberedChT","tomListNumberedCircle","tomListNumberedHebrew","tomListNumberedHindiAlpha","tomListNumberedHindiAlpha1","tomListNumberedHindiNum","tomListNumberedJpnChs","tomListNumberedJpnKor","tomListNumberedThaiAlpha","tomListNumberedThaiNum","tomListNumberedWhiteCircleWingding","tomListParentheses","tomListPeriod","tomListPlain"]
old-location: controls\ITextPara_GetListType.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlisttype.htm
ms.date: 12/05/2018
ms.keywords: GetListType, GetListType method [Windows Controls], GetListType method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetListType method, ITextPara.GetListType, ITextPara::GetListType, _win32_ITextPara_GetListType, _win32_ITextPara_GetListType_cpp, controls.ITextPara_GetListType, controls._win32_ITextPara_GetListType, tom/ITextPara::GetListType, tomListBullet, tomListMinus, tomListNone, tomListNumberAsArabic, tomListNumberAsLCLetter, tomListNumberAsLCRoman, tomListNumberAsSequence, tomListNumberAsUCLetter, tomListNumberAsUCRoman, tomListNumberedArabic1, tomListNumberedArabic2, tomListNumberedArabicWide, tomListNumberedBlackCircleWingding, tomListNumberedChS, tomListNumberedChT, tomListNumberedCircle, tomListNumberedHebrew, tomListNumberedHindiAlpha, tomListNumberedHindiAlpha1, tomListNumberedHindiNum, tomListNumberedJpnChs, tomListNumberedJpnKor, tomListNumberedThaiAlpha, tomListNumberedThaiNum, tomListNumberedWhiteCircleWingding, tomListParentheses, tomListPeriod, tomListPlain
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
 - ITextPara::GetListType
 - tom/ITextPara::GetListType
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
 - ITextPara.GetListType
---

# ITextPara::GetListType


## -description

Retrieves the kind of numbering to use with paragraphs.

## -parameters

### -param pValue

Type: <b>long*</b>

A variable that is of the following values to indicate the kind of list numbering. 
					

<a id="tomListNone"></a>
<a id="tomlistnone"></a>
<a id="TOMLISTNONE"></a>


#### tomListNone

<a id="tomListBullet"></a>
<a id="tomlistbullet"></a>
<a id="TOMLISTBULLET"></a>


#### tomListBullet

<a id="tomListNumberAsArabic"></a>
<a id="tomlistnumberasarabic"></a>
<a id="TOMLISTNUMBERASARABIC"></a>


#### tomListNumberAsArabic

<a id="tomListNumberAsLCLetter"></a>
<a id="tomlistnumberaslcletter"></a>
<a id="TOMLISTNUMBERASLCLETTER"></a>


#### tomListNumberAsLCLetter

<a id="tomListNumberAsUCLetter"></a>
<a id="tomlistnumberasucletter"></a>
<a id="TOMLISTNUMBERASUCLETTER"></a>


#### tomListNumberAsUCLetter

<a id="tomListNumberAsLCRoman"></a>
<a id="tomlistnumberaslcroman"></a>
<a id="TOMLISTNUMBERASLCROMAN"></a>


#### tomListNumberAsLCRoman

<a id="tomListNumberAsUCRoman"></a>
<a id="tomlistnumberasucroman"></a>
<a id="TOMLISTNUMBERASUCROMAN"></a>


#### tomListNumberAsUCRoman

<a id="tomListNumberAsSequence"></a>
<a id="tomlistnumberassequence"></a>
<a id="TOMLISTNUMBERASSEQUENCE"></a>


#### tomListNumberAsSequence

<a id="tomListNumberedCircle"></a>
<a id="tomlistnumberedcircle"></a>
<a id="TOMLISTNUMBEREDCIRCLE"></a>


#### tomListNumberedCircle

<a id="tomListNumberedBlackCircleWingding"></a>
<a id="tomlistnumberedblackcirclewingding"></a>
<a id="TOMLISTNUMBEREDBLACKCIRCLEWINGDING"></a>


#### tomListNumberedBlackCircleWingding

<a id="tomListNumberedWhiteCircleWingding"></a>
<a id="tomlistnumberedwhitecirclewingding"></a>
<a id="TOMLISTNUMBEREDWHITECIRCLEWINGDING"></a>


#### tomListNumberedWhiteCircleWingding

<a id="tomListNumberedArabicWide"></a>
<a id="tomlistnumberedarabicwide"></a>
<a id="TOMLISTNUMBEREDARABICWIDE"></a>


#### tomListNumberedArabicWide

<a id="tomListNumberedChS"></a>
<a id="tomlistnumberedchs"></a>
<a id="TOMLISTNUMBEREDCHS"></a>


#### tomListNumberedChS

<a id="tomListNumberedChT"></a>
<a id="tomlistnumberedcht"></a>
<a id="TOMLISTNUMBEREDCHT"></a>


#### tomListNumberedChT

<a id="tomListNumberedJpnChs"></a>
<a id="tomlistnumberedjpnchs"></a>
<a id="TOMLISTNUMBEREDJPNCHS"></a>


#### tomListNumberedJpnChs

<a id="tomListNumberedJpnKor"></a>
<a id="tomlistnumberedjpnkor"></a>
<a id="TOMLISTNUMBEREDJPNKOR"></a>


#### tomListNumberedJpnKor

<a id="tomListNumberedArabic1"></a>
<a id="tomlistnumberedarabic1"></a>
<a id="TOMLISTNUMBEREDARABIC1"></a>


#### tomListNumberedArabic1

<a id="tomListNumberedArabic2"></a>
<a id="tomlistnumberedarabic2"></a>
<a id="TOMLISTNUMBEREDARABIC2"></a>


#### tomListNumberedArabic2

<a id="tomListNumberedHebrew"></a>
<a id="tomlistnumberedhebrew"></a>
<a id="TOMLISTNUMBEREDHEBREW"></a>


#### tomListNumberedHebrew

<a id="tomListNumberedThaiAlpha"></a>
<a id="tomlistnumberedthaialpha"></a>
<a id="TOMLISTNUMBEREDTHAIALPHA"></a>


#### tomListNumberedThaiAlpha

<a id="tomListNumberedThaiNum"></a>
<a id="tomlistnumberedthainum"></a>
<a id="TOMLISTNUMBEREDTHAINUM"></a>


#### tomListNumberedThaiNum

<a id="tomListNumberedHindiAlpha"></a>
<a id="tomlistnumberedhindialpha"></a>
<a id="TOMLISTNUMBEREDHINDIALPHA"></a>


#### tomListNumberedHindiAlpha

<a id="tomListNumberedHindiAlpha1"></a>
<a id="tomlistnumberedhindialpha1"></a>
<a id="TOMLISTNUMBEREDHINDIALPHA1"></a>


#### tomListNumberedHindiAlpha1

<a id="tomListNumberedHindiNum"></a>
<a id="tomlistnumberedhindinum"></a>
<a id="TOMLISTNUMBEREDHINDINUM"></a>


#### tomListNumberedHindiNum

By default, numbers are followed by a right parenthesis, for example: 1). However,  <i>pValue</i> can include one of the following flags to indicate a different formatting. 
					
				

<a id="tomListMinus"></a>
<a id="tomlistminus"></a>
<a id="TOMLISTMINUS"></a>


#### tomListMinus

<a id="tomListParentheses"></a>
<a id="tomlistparentheses"></a>
<a id="TOMLISTPARENTHESES"></a>


#### tomListParentheses

<a id="tomListPeriod"></a>
<a id="tomlistperiod"></a>
<a id="TOMLISTPERIOD"></a>


#### tomListPeriod

<a id="tomListPlain"></a>
<a id="tomlistplain"></a>
<a id="TOMLISTPLAIN"></a>


#### tomListPlain

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If <b>ITextPara::GetListType</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -remarks

Values above 32 correspond to Unicode values for bullets. 

The mobile Microsoft Office version of the rich edit control uses <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomIgnoreNumberStyle</a> to suppress setting the style.

The following Microsoft Visual Basic for Applications (VBA) example numbers the paragraphs in a range, starting with the number 2 and following the numbers with a period.
            


```
    range.Para.ListStart = 2
    range.Para.ListType = tomListNumberAsArabic + tomListPeriod
```


For an example of <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomListNumberAsSequence</a>, set <code>ListStart</code> to 0x2780, which gives you circled numbers. The <a href="https://www.unicode.org/standard/standard.html">Unicode Standard</a> has examples of many more numbering sequences.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getliststart">GetListStart</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setliststart">SetListStart</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttype">SetListType</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>