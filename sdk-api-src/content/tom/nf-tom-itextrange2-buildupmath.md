---
UID: NF:tom.ITextRange2.BuildUpMath
title: ITextRange2::BuildUpMath (tom.h)
description: Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.
helpviewer_keywords: ["BuildUpMath","BuildUpMath method [Windows Controls]","BuildUpMath method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","BuildUpMath method","ITextRange2.BuildUpMath","ITextRange2::BuildUpMath","controls.itextrange2_buildupmath","tom/ITextRange2::BuildUpMath","tomChemicalFormula","tomHaveDelimiter","tomMathAlphabetics","tomMathApplyTemplate","tomMathArabicAlphabetics","tomMathAutoCorrect","tomMathAutoCorrectExt","tomMathAutoCorrectOpPairs","tomMathBackspace","tomMathBuildDown","tomMathBuildDownOutermost","tomMathBuildUpArgOrZone","tomMathBuildUpRecurse","tomMathChangeMask","tomMathCollapseSel","tomMathDeleteArg","tomMathDeleteArg1","tomMathDeleteArg2","tomMathDeleteCol","tomMathDeleteRow","tomMathEnter","tomMathInsColAfter","tomMathInsColBefore","tomMathInsRowAfter","tomMathInsRowBefore","tomMathMakeFracLinear","tomMathMakeFracSlashed","tomMathMakeFracStacked","tomMathMakeLeftSubSup","tomMathMakeSubSup","tomMathRemoveOutermost","tomMathRichEdit","tomMathShiftTab","tomMathSingleChar","tomMathSubscript","tomMathSuperscript","tomMathTab","tomNeedTermOp","tomPlain","tomShowEmptyArgPlaceholders","tomTeX"]
old-location: controls\itextrange2_buildupmath.htm
tech.root: Controls
ms.assetid: b6382f09-126e-4107-a4b9-288777549181
ms.date: 12/05/2018
ms.keywords: BuildUpMath, BuildUpMath method [Windows Controls], BuildUpMath method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],BuildUpMath method, ITextRange2.BuildUpMath, ITextRange2::BuildUpMath, controls.itextrange2_buildupmath, tom/ITextRange2::BuildUpMath, tomChemicalFormula, tomHaveDelimiter, tomMathAlphabetics, tomMathApplyTemplate, tomMathArabicAlphabetics, tomMathAutoCorrect, tomMathAutoCorrectExt, tomMathAutoCorrectOpPairs, tomMathBackspace, tomMathBuildDown, tomMathBuildDownOutermost, tomMathBuildUpArgOrZone, tomMathBuildUpRecurse, tomMathChangeMask, tomMathCollapseSel, tomMathDeleteArg, tomMathDeleteArg1, tomMathDeleteArg2, tomMathDeleteCol, tomMathDeleteRow, tomMathEnter, tomMathInsColAfter, tomMathInsColBefore, tomMathInsRowAfter, tomMathInsRowBefore, tomMathMakeFracLinear, tomMathMakeFracSlashed, tomMathMakeFracStacked, tomMathMakeLeftSubSup, tomMathMakeSubSup, tomMathRemoveOutermost, tomMathRichEdit, tomMathShiftTab, tomMathSingleChar, tomMathSubscript, tomMathSuperscript, tomMathTab, tomNeedTermOp, tomPlain, tomShowEmptyArgPlaceholders, tomTeX
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
 - ITextRange2::BuildUpMath
 - tom/ITextRange2::BuildUpMath
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
 - ITextRange2.BuildUpMath
---

# ITextRange2::BuildUpMath


## -description

Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.

## -parameters

### -param Flags [in]

Type: <b>long</b>

A combination of the following flags.

<a id="tomChemicalFormula"></a>
<a id="tomchemicalformula"></a>
<a id="TOMCHEMICALFORMULA"></a>


#### tomChemicalFormula

<a id="tomHaveDelimiter"></a>
<a id="tomhavedelimiter"></a>
<a id="TOMHAVEDELIMITER"></a>


#### tomHaveDelimiter

<a id="tomMathAlphabetics_"></a>
<a id="tommathalphabetics_"></a>
<a id="TOMMATHALPHABETICS_"></a>


#### tomMathAlphabetics

<a id="tomMathApplyTemplate"></a>
<a id="tommathapplytemplate"></a>
<a id="TOMMATHAPPLYTEMPLATE"></a>


#### tomMathApplyTemplate

<a id="tomMathArabicAlphabetics____"></a>
<a id="tommatharabicalphabetics____"></a>
<a id="TOMMATHARABICALPHABETICS____"></a>


#### tomMathArabicAlphabetics

<a id="tomMathAutoCorrect"></a>
<a id="tommathautocorrect"></a>
<a id="TOMMATHAUTOCORRECT"></a>


#### tomMathAutoCorrect

<a id="tomMathAutoCorrectExt"></a>
<a id="tommathautocorrectext"></a>
<a id="TOMMATHAUTOCORRECTEXT"></a>


#### tomMathAutoCorrectExt

<a id="tomMathAutoCorrectOpPairs"></a>
<a id="tommathautocorrectoppairs"></a>
<a id="TOMMATHAUTOCORRECTOPPAIRS"></a>


#### tomMathAutoCorrectOpPairs

<a id="tomMathBackspace"></a>
<a id="tommathbackspace"></a>
<a id="TOMMATHBACKSPACE"></a>


#### tomMathBackspace

<a id="tomMathBuildDown"></a>
<a id="tommathbuilddown"></a>
<a id="TOMMATHBUILDDOWN"></a>


#### tomMathBuildDown

<a id="tomMathBuildDownOutermost"></a>
<a id="tommathbuilddownoutermost"></a>
<a id="TOMMATHBUILDDOWNOUTERMOST"></a>


#### tomMathBuildDownOutermost

<a id="tomMathBuildUpArgOrZone_"></a>
<a id="tommathbuildupargorzone_"></a>
<a id="TOMMATHBUILDUPARGORZONE_"></a>


#### tomMathBuildUpArgOrZone

<a id="tomMathBuildUpRecurse"></a>
<a id="tommathbuilduprecurse"></a>
<a id="TOMMATHBUILDUPRECURSE"></a>


#### tomMathBuildUpRecurse

<a id="tomMathChangeMask"></a>
<a id="tommathchangemask"></a>
<a id="TOMMATHCHANGEMASK"></a>


#### tomMathChangeMask

<a id="tomMathCollapseSel"></a>
<a id="tommathcollapsesel"></a>
<a id="TOMMATHCOLLAPSESEL"></a>


#### tomMathCollapseSel

<a id="tomMathDeleteArg"></a>
<a id="tommathdeletearg"></a>
<a id="TOMMATHDELETEARG"></a>


#### tomMathDeleteArg

<a id="tomMathDeleteArg1"></a>
<a id="tommathdeletearg1"></a>
<a id="TOMMATHDELETEARG1"></a>


#### tomMathDeleteArg1

<a id="tomMathDeleteArg2"></a>
<a id="tommathdeletearg2"></a>
<a id="TOMMATHDELETEARG2"></a>


#### tomMathDeleteArg2

<a id="tomMathDeleteCol"></a>
<a id="tommathdeletecol"></a>
<a id="TOMMATHDELETECOL"></a>


#### tomMathDeleteCol

<a id="tomMathDeleteRow"></a>
<a id="tommathdeleterow"></a>
<a id="TOMMATHDELETEROW"></a>


#### tomMathDeleteRow

<a id="tomMathEnter"></a>
<a id="tommathenter"></a>
<a id="TOMMATHENTER"></a>


#### tomMathEnter

<a id="tomMathInsColAfter"></a>
<a id="tommathinscolafter"></a>
<a id="TOMMATHINSCOLAFTER"></a>


#### tomMathInsColAfter

<a id="tomMathInsColBefore"></a>
<a id="tommathinscolbefore"></a>
<a id="TOMMATHINSCOLBEFORE"></a>


#### tomMathInsColBefore

<a id="tomMathInsRowAfter"></a>
<a id="tommathinsrowafter"></a>
<a id="TOMMATHINSROWAFTER"></a>


#### tomMathInsRowAfter

<a id="tomMathInsRowBefore"></a>
<a id="tommathinsrowbefore"></a>
<a id="TOMMATHINSROWBEFORE"></a>


#### tomMathInsRowBefore

<a id="tomMathMakeFracLinear_"></a>
<a id="tommathmakefraclinear_"></a>
<a id="TOMMATHMAKEFRACLINEAR_"></a>


#### tomMathMakeFracLinear

<a id="tomMathMakeFracSlashed"></a>
<a id="tommathmakefracslashed"></a>
<a id="TOMMATHMAKEFRACSLASHED"></a>


#### tomMathMakeFracSlashed

<a id="tomMathMakeFracStacked"></a>
<a id="tommathmakefracstacked"></a>
<a id="TOMMATHMAKEFRACSTACKED"></a>


#### tomMathMakeFracStacked

<a id="tomMathMakeLeftSubSup"></a>
<a id="tommathmakeleftsubsup"></a>
<a id="TOMMATHMAKELEFTSUBSUP"></a>


#### tomMathMakeLeftSubSup

<a id="tomMathMakeSubSup"></a>
<a id="tommathmakesubsup"></a>
<a id="TOMMATHMAKESUBSUP"></a>


#### tomMathMakeSubSup

<a id="tomMathRemoveOutermost"></a>
<a id="tommathremoveoutermost"></a>
<a id="TOMMATHREMOVEOUTERMOST"></a>


#### tomMathRemoveOutermost

<a id="tomMathRichEdit"></a>
<a id="tommathrichedit"></a>
<a id="TOMMATHRICHEDIT"></a>


#### tomMathRichEdit

<a id="tomMathShiftTab"></a>
<a id="tommathshifttab"></a>
<a id="TOMMATHSHIFTTAB"></a>


#### tomMathShiftTab

<a id="tomMathSingleChar_"></a>
<a id="tommathsinglechar_"></a>
<a id="TOMMATHSINGLECHAR_"></a>


#### tomMathSingleChar

<a id="tomMathSubscript"></a>
<a id="tommathsubscript"></a>
<a id="TOMMATHSUBSCRIPT"></a>


#### tomMathSubscript

<a id="tomMathSuperscript"></a>
<a id="tommathsuperscript"></a>
<a id="TOMMATHSUPERSCRIPT"></a>


#### tomMathSuperscript

<a id="tomMathTab"></a>
<a id="tommathtab"></a>
<a id="TOMMATHTAB"></a>


#### tomMathTab

<a id="tomNeedTermOp"></a>
<a id="tomneedtermop"></a>
<a id="TOMNEEDTERMOP"></a>


#### tomNeedTermOp

<a id="tomPlain"></a>
<a id="tomplain"></a>
<a id="TOMPLAIN"></a>


#### tomPlain

<a id="tomShowEmptyArgPlaceholders"></a>
<a id="tomshowemptyargplaceholders"></a>
<a id="TOMSHOWEMPTYARGPLACEHOLDERS"></a>


#### tomShowEmptyArgPlaceholders

<a id="tomTeX_"></a>
<a id="tomtex_"></a>
<a id="TOMTEX_"></a>


#### tomTeX

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <b>ITextRange2::BuildUpMath</b> method is called on a nondegenerate range, the method checks the text for math italic conversions (if <b>tomMathAlphabetics</b> is specified) and math autocorrect conversions (if <b>tomMathAutoCorrect</b> or <b>tomMathAutoCorrectExt</b> is specified). Then, the method attempts to build up the selected text. If successful, the method replaces the previous text in the range with the built-up text. If the method makes any changes to the range, the function returns <b>NOERROR</b> and the range selects the result. If the method does change the range, it returns <b>S_FALSE</b> or a Component Object Model (COM) error code.


If the <b>ITextRange2::BuildUpMath</b> method is called on a degenerate range, the <b>BuildUpMath</b> method treats the range as an insertion point (IP) immediately following the last character input. The method converts that character, possibly along with some preceding characters, to math italic (if <b>tomMathAlphabetics</b> is specified), internal math autocorrect (if <b>tomMathAutoCorrect</b> is specified), negated operators, and some operator pairs  (if <b>tomMathAutoCorrectOpPairs</b> is specified). If the IP is inside an argument, the method scans a range of text from the IP back to the start of a math object argument; otherwise, the method scans to the start of the current math zone. The scan is terminated by a hard carriage return or a soft end-of-paragraph mark, because math zones are terminated by these marks. A scan forward from start of the math object argument or math zone bypasses text that has no chance of being built up. If the scan reaches the original entry IP, one of the following outcomes can occur:


<ul>
<li>If the method made any changes, the function returns <b>NOERROR</b> and the range updated with the changed text.</li>
<li>If the method made no changes, the function returns <b>S_FALSE</b> and leaves the range unchanged.
</li>
</ul>
If the scan finds text that might get built up, the <b>BuildUpMath</b> method attempts to build up the text up to the insertion point. If successful, the method returns <b>NOERROR</b>, and the range is updated with the corresponding built-up text. 


If this full build-up attempt fails, the <b>BuildUpMath</b> method does a partial build-up check for the expression immediately preceding the IP. If this succeeds, the method returns <b>NOERROR</b> and the range contains the linear text to be replaced by the built-up text.


If full and partial build-up attempts fail, the function returns as described previously for the cases where no build-up text was found. Other possible return values include <b>E_INVALIDARG</b> (if either interface pointer is <b>NULL</b>) and <b>E_OUTOFMEMORY</b>. 


You should set the <b>tomNeedTermOp</b> flag should for formula autobuildup unless autocorrection has occurred that deletes the terminating blank. Autocorrection can occur when correcting text like \alpha when the user types a blank to force autocorrection.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-linearize">ITextRange2::Linearize</a>