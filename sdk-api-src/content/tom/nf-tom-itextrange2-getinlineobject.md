---
UID: NF:tom.ITextRange2.GetInlineObject
title: ITextRange2::GetInlineObject (tom.h)
description: Gets the properties of the inline object at the range active end.
helpviewer_keywords: ["GetInlineObject","GetInlineObject method [Windows Controls]","GetInlineObject method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetInlineObject method","ITextRange2.GetInlineObject","ITextRange2::GetInlineObject","controls.itextrange2_getinlineobject","tom/ITextRange2::GetInlineObject","tomAccent","tomBox","tomBoxedFormula","tomBrackets","tomBracketsWithSeps","tomEquationArray","tomFraction","tomFunctionApply","tomHorzVert","tomLeftSubSup","tomLowerLimit","tomMatrix","tomNary","tomOpChar","tomOverbar","tomPhantom","tomRadical","tomRuby","tomSimpleText","tomSlashedFraction","tomStack","tomStretchStack","tomStyleDefault","tomStyleDisplay","tomStyleDisplayCramped","tomStyleScript","tomStyleScriptCramped","tomStyleScriptScript","tomStyleScriptScriptCramped","tomStyleText","tomStyleTextCramped","tomSubSup","tomSubscript","tomSuperscript","tomUnderbar","tomUpperLimit","tomWarichu"]
old-location: controls\itextrange2_getinlineobject.htm
tech.root: Controls
ms.assetid: 0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56
ms.date: 12/05/2018
ms.keywords: GetInlineObject, GetInlineObject method [Windows Controls], GetInlineObject method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetInlineObject method, ITextRange2.GetInlineObject, ITextRange2::GetInlineObject, controls.itextrange2_getinlineobject, tom/ITextRange2::GetInlineObject, tomAccent, tomBox, tomBoxedFormula, tomBrackets, tomBracketsWithSeps, tomEquationArray, tomFraction, tomFunctionApply, tomHorzVert, tomLeftSubSup, tomLowerLimit, tomMatrix, tomNary, tomOpChar, tomOverbar, tomPhantom, tomRadical, tomRuby, tomSimpleText, tomSlashedFraction, tomStack, tomStretchStack, tomStyleDefault, tomStyleDisplay, tomStyleDisplayCramped, tomStyleScript, tomStyleScriptCramped, tomStyleScriptScript, tomStyleScriptScriptCramped, tomStyleText, tomStyleTextCramped, tomSubSup, tomSubscript, tomSuperscript, tomUnderbar, tomUpperLimit, tomWarichu
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
 - ITextRange2::GetInlineObject
 - tom/ITextRange2::GetInlineObject
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
 - ITextRange2.GetInlineObject
---

# ITextRange2::GetInlineObject


## -description

Gets the properties of the inline object at the range active end.

## -parameters

### -param pType [out]

Type: <b>long*</b>

The inline object type can be one of the following:


<a id="tomSimpleText"></a>
<a id="tomsimpletext"></a>
<a id="TOMSIMPLETEXT"></a>


#### tomSimpleText

<a id="tomRuby"></a>
<a id="tomruby"></a>
<a id="TOMRUBY"></a>


#### tomRuby

<a id="tomHorzVert"></a>
<a id="tomhorzvert"></a>
<a id="TOMHORZVERT"></a>


#### tomHorzVert

<a id="tomWarichu"></a>
<a id="tomwarichu"></a>
<a id="TOMWARICHU"></a>


#### tomWarichu

<a id="tomAccent"></a>
<a id="tomaccent"></a>
<a id="TOMACCENT"></a>


#### tomAccent

<a id="tomBox"></a>
<a id="tombox"></a>
<a id="TOMBOX"></a>


#### tomBox

<a id="tomBoxedFormula"></a>
<a id="tomboxedformula"></a>
<a id="TOMBOXEDFORMULA"></a>


#### tomBoxedFormula

<a id="tomBrackets"></a>
<a id="tombrackets"></a>
<a id="TOMBRACKETS"></a>


#### tomBrackets

<a id="tomBracketsWithSeps"></a>
<a id="tombracketswithseps"></a>
<a id="TOMBRACKETSWITHSEPS"></a>


#### tomBracketsWithSeps

<a id="tomEquationArray"></a>
<a id="tomequationarray"></a>
<a id="TOMEQUATIONARRAY"></a>


#### tomEquationArray

<a id="tomFraction"></a>
<a id="tomfraction"></a>
<a id="TOMFRACTION"></a>


#### tomFraction

<a id="tomFunctionApply"></a>
<a id="tomfunctionapply"></a>
<a id="TOMFUNCTIONAPPLY"></a>


#### tomFunctionApply

<a id="tomLeftSubSup"></a>
<a id="tomleftsubsup"></a>
<a id="TOMLEFTSUBSUP"></a>


#### tomLeftSubSup

<a id="tomLowerLimit"></a>
<a id="tomlowerlimit"></a>
<a id="TOMLOWERLIMIT"></a>


#### tomLowerLimit

<a id="tomMatrix"></a>
<a id="tommatrix"></a>
<a id="TOMMATRIX"></a>


#### tomMatrix

<a id="tomNary"></a>
<a id="tomnary"></a>
<a id="TOMNARY"></a>


#### tomNary

<a id="tomOpChar"></a>
<a id="tomopchar"></a>
<a id="TOMOPCHAR"></a>


#### tomOpChar

<a id="tomOverbar"></a>
<a id="tomoverbar"></a>
<a id="TOMOVERBAR"></a>


#### tomOverbar

<a id="tomPhantom"></a>
<a id="tomphantom"></a>
<a id="TOMPHANTOM"></a>


#### tomPhantom

<a id="tomRadical"></a>
<a id="tomradical"></a>
<a id="TOMRADICAL"></a>


#### tomRadical

<a id="tomSlashedFraction"></a>
<a id="tomslashedfraction"></a>
<a id="TOMSLASHEDFRACTION"></a>


#### tomSlashedFraction

<a id="tomStack"></a>
<a id="tomstack"></a>
<a id="TOMSTACK"></a>


#### tomStack

<a id="tomStretchStack"></a>
<a id="tomstretchstack"></a>
<a id="TOMSTRETCHSTACK"></a>


#### tomStretchStack

<a id="tomSubscript"></a>
<a id="tomsubscript"></a>
<a id="TOMSUBSCRIPT"></a>


#### tomSubscript

<a id="tomSubSup"></a>
<a id="tomsubsup"></a>
<a id="TOMSUBSUP"></a>


#### tomSubSup

<a id="tomSuperscript"></a>
<a id="tomsuperscript"></a>
<a id="TOMSUPERSCRIPT"></a>


#### tomSuperscript

<a id="tomUnderbar"></a>
<a id="tomunderbar"></a>
<a id="TOMUNDERBAR"></a>


#### tomUnderbar

<a id="tomUpperLimit"></a>
<a id="tomupperlimit"></a>
<a id="TOMUPPERLIMIT"></a>


#### tomUpperLimit

### -param pAlign [out]

Type: <b>long*</b>

The inline object alignment, which can be one of these meanings depending on the inline object type:
<table>
<tr>
<th>Inline object type</th>
<th>Meaning of Align Parameter</th>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomRuby</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomRubyBelow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomRubyAlignCenter</a> (default)</dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomRubyAlign010</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomRubyAlign121</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomRubyAlignLeft</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomRubyAlignRight</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomBox</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxAlignCenter</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceMask</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceDefault</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceUnary</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceBinary</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceRelational</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceSkip</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceOrd</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSpaceDifferential</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSizeText</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSizeScript</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSizeScriptScript</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomNoBreak</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomTransparentForPositioning</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomTransparentForSpacing</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomBoxedFormula</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxHideTop</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxHideBottom</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxHideLeft</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxHideRight</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxStrikeH</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxStrikeV</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxStrikeTLBR</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBoxStrikeBLTR</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomBrackets</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignDefault</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignCenter</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignMatchAscentDescent</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathVariant</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomEquationArray</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomEqArrayLayoutWidth</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomEqArrayAlignMask</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomEqArrayAlignCenter</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomEqArrayAlignTopRow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomEqArrayAlignBottomRow</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomMatrix</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMatrixAlignMask</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMatrixAlignCenter</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMatrixAlignTopRow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMatrixAlignBottomRow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomShowMatPlaceHldr</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomNary</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomLimitsDefault</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomLimitsUnderOver</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomLimitsSubSup</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUpperLimitAsSuperScript</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomLimitsOpposite</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomShowLLimPlaceHldr</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomShowULimPlaceHldr</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomDontGrowWithContent</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomGrowWithContent</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomPhantom</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomPhantomShow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomPhantomZeroWidth</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomPhantomZeroAscent</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomPhantomZeroDescent</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomPhantomTransparent</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomRadical</a></td>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomShowDegPlaceHldr</a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomSubSup</a></td>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSubSupAlign</a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomStretchStack</a></td>
<td>
<dl>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomStretchCharBelow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomStretchCharAbove</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomStretchBaseBelow</a></dt>
<dt><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomStretchBaseAbove</a></dt>
</dl>
</td>
</tr>
</table>

### -param pChar [out]

Type: <b>long*</b>

The inline object character.

The value for each object type is shown in the following table..  <table>
<tr>
<th>Inline object type</th>
<th>Meaning of align parameter</th>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomAccent</a></td>
<td>Accent (U+0300—U+36F, U+20D0—U+20EF)</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomBoxedFormula</a></td>
<td>U+25AD for rectangle enclosure</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomBrackets</a></td>
<td>Opening bracket. Default: U+0028.  </td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomBracketsWithSeps</a></td>
<td>Opening bracket with separators. Default: U+0028</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomEquationArray</a></td>
<td>U+2588</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomFraction</a></td>
<td>Normal built-up fraction: U+002F; small numeric fraction: U+2298</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomFunctionApply</a></td>
<td>U+2061</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomLeftSubSup</a></td>
<td>U+005E</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomLowerLimit</a></td>
<td>U+252C</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomMatrix</a></td>
<td>
<dl>
<dt>U+25A0: no enclosing brackets
</dt>
<dt>U+24A8: enclosing parentheses (\pmatrix)
</dt>
<dt>U+24B1: enclosing vertical bars (\vmatrix)
</dt>
<dt>U+24A9: enclosing double vertical bars (\Vmatrix)
</dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomNary</a></td>
<td>n-ary symbol</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomOpChar</a></td>
<td>Internal use for no-build operators</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomOverbar</a></td>
<td>U+00AF</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomPhantom</a></td>
<td>
<dl>
<dt>U+27E1: full or custom phantom
</dt>
<dt>U+2B04: horizontal phantom
</dt>
<dt>U+21F3: vertical phantom
</dt>
<dt>U+2B06: ascent smash
</dt>
<dt>U+2B07: descent smash
</dt>
<dt>U+2B0C: horizontal smash
</dt>
<dt>U+2B0D: full smash
</dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomRadical</a></td>
<td>
<dl>
<dt>U+221A: square or nth root
</dt>
<dt>U+221B: cube root
</dt>
<dt>U+221C: fourth root
</dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomSlashedFraction</a></td>
<td>
<dl>
<dt>U+2044: skewed fraction</dt>
<dt>U+2215: built-up linear fraction
</dt>
</dl>
</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomStack</a></td>
<td>U+00A6

</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomStretchStack</a></td>
<td>Horizontal stretch character (see <a href="https://www.unicode.org/notes/tn28/">Unicode Technical Note 28</a> Appendix B for a list)</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomSubscript</a></td>
<td>U+005E




</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomSubSup</a></td>
<td>U+005E</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomSuperscript</a></td>
<td>U+005F</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomUnderbar</a></td>
<td>U+2581</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-objecttype">tomUpperLimit</a></td>
<td>U+2534</td>
</tr>
</table>

### -param pChar1 [out]

Type: <b>long*</b>

The closing <b>tomBrackets</b> character.  See <a href="https://www.unicode.org/notes/tn28/">Unicode Technical Note 28</a> Appendix B. Character Keywords and Properties for a list.

### -param pChar2 [out]

Type: <b>long*</b>

The separator character for <b>tomBracketsWithSep</b>:



#### U+007C: vertical bar with no extra spacing



#### U+2223: vertical bar with extra spacing

### -param pCount [out]

Type: <b>long*</b>

The inline object count of arguments.

### -param pTeXStyle [out]

Type: <b>long*</b>


The inline object TeX style, which can be one of the following values. 


<div class="alert"><b>Note</b>  The <b>tomStyleDefault</b> behavior depends on the context.</div>
<div> </div>


<a id="tomStyleDefault"></a>
<a id="tomstyledefault"></a>
<a id="TOMSTYLEDEFAULT"></a>


#### tomStyleDefault

<a id="tomStyleScriptScriptCramped"></a>
<a id="tomstylescriptscriptcramped"></a>
<a id="TOMSTYLESCRIPTSCRIPTCRAMPED"></a>


#### tomStyleScriptScriptCramped

<a id="tomStyleScriptScript"></a>
<a id="tomstylescriptscript"></a>
<a id="TOMSTYLESCRIPTSCRIPT"></a>


#### tomStyleScriptScript

<a id="tomStyleScriptCramped"></a>
<a id="tomstylescriptcramped"></a>
<a id="TOMSTYLESCRIPTCRAMPED"></a>


#### tomStyleScriptCramped

<a id="tomStyleScript"></a>
<a id="tomstylescript"></a>
<a id="TOMSTYLESCRIPT"></a>


#### tomStyleScript

<a id="tomStyleTextCramped"></a>
<a id="tomstyletextcramped"></a>
<a id="TOMSTYLETEXTCRAMPED"></a>


#### tomStyleTextCramped

<a id="tomStyleText"></a>
<a id="tomstyletext"></a>
<a id="TOMSTYLETEXT"></a>


#### tomStyleText

<a id="tomStyleDisplayCramped"></a>
<a id="tomstyledisplaycramped"></a>
<a id="TOMSTYLEDISPLAYCRAMPED"></a>


#### tomStyleDisplayCramped

<a id="tomStyleDisplay"></a>
<a id="tomstyledisplay"></a>
<a id="TOMSTYLEDISPLAY"></a>


#### tomStyleDisplay

### -param pcCol [out]

Type: <b>long*</b>

The inline object count of columns (<b>tomMatrix</b> only).

### -param pLevel [out]

Type: <b>long*</b>

The inline object 0-based nesting level.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="https://www.unicode.org/notes/tn28/">Unicode Technical Note 28</a> describes the alignment and character values in detail when the active end character is an inline object start delimiter. 

When that character is not a start delimiter, the character and column parameters are set to 0, the count is set to the 0-based argument index, and the other parameters are set according to the active-end character properties of the innermost inline object argument.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setinlineobject">ITextRange2::SetInlineObject</a>