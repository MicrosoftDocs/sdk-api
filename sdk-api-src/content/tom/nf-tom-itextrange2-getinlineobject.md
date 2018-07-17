---
UID: NF:tom.ITextRange2.GetInlineObject
title: ITextRange2::GetInlineObject
author: windows-sdk-content
description: Gets the properties of the inline object at the range active end.
old-location: controls\itextrange2_getinlineobject.htm
old-project: Controls
ms.assetid: 0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetInlineObject, GetInlineObject method [Windows Controls], GetInlineObject method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetInlineObject method, ITextRange2.GetInlineObject, ITextRange2::GetInlineObject, controls.itextrange2_getinlineobject, tom/ITextRange2::GetInlineObject, tomAccent, tomBox, tomBoxedFormula, tomBrackets, tomBracketsWithSeps, tomEquationArray, tomFraction, tomFunctionApply, tomHorzVert, tomLeftSubSup, tomLowerLimit, tomMatrix, tomNary, tomOpChar, tomOverbar, tomPhantom, tomRadical, tomRuby, tomSimpleText, tomSlashedFraction, tomStack, tomStretchStack, tomStyleDefault, tomStyleDisplay, tomStyleDisplayCramped, tomStyleScript, tomStyleScriptCramped, tomStyleScriptScript, tomStyleScriptScriptCramped, tomStyleText, tomStyleTextCramped, tomSubSup, tomSubscript, tomSuperscript, tomUnderbar, tomUpperLimit, tomWarichu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.GetInlineObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<td><a href="objecttype.htm">tomRuby</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomRubyBelow</a></dt>
<dt><a href="tomconstants.htm">tomRubyAlignCenter</a> (default)</dt>
<dt><a href="tomconstants.htm">tomRubyAlign010</a></dt>
<dt><a href="tomconstants.htm">tomRubyAlign121</a></dt>
<dt><a href="tomconstants.htm">tomRubyAlignLeft</a></dt>
<dt><a href="tomconstants.htm">tomRubyAlignRight</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomBox</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomBoxAlignCenter</a></dt>
<dt><a href="tomconstants.htm">tomSpaceMask</a></dt>
<dt><a href="tomconstants.htm">tomSpaceDefault</a></dt>
<dt><a href="tomconstants.htm">tomSpaceUnary</a></dt>
<dt><a href="tomconstants.htm">tomSpaceBinary</a></dt>
<dt><a href="tomconstants.htm">tomSpaceRelational</a></dt>
<dt><a href="tomconstants.htm">tomSpaceSkip</a></dt>
<dt><a href="tomconstants.htm">tomSpaceOrd</a></dt>
<dt><a href="tomconstants.htm">tomSpaceDifferential</a></dt>
<dt><a href="tomconstants.htm">tomSizeText</a></dt>
<dt><a href="tomconstants.htm">tomSizeScript</a></dt>
<dt><a href="tomconstants.htm">tomSizeScriptScript</a></dt>
<dt><a href="tomconstants.htm">tomNoBreak</a></dt>
<dt><a href="tomconstants.htm">tomTransparentForPositioning</a></dt>
<dt><a href="tomconstants.htm">tomTransparentForSpacing</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomBoxedFormula</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomBoxHideTop</a></dt>
<dt><a href="tomconstants.htm">tomBoxHideBottom</a></dt>
<dt><a href="tomconstants.htm">tomBoxHideLeft</a></dt>
<dt><a href="tomconstants.htm">tomBoxHideRight</a></dt>
<dt><a href="tomconstants.htm">tomBoxStrikeH</a></dt>
<dt><a href="tomconstants.htm">tomBoxStrikeV</a></dt>
<dt><a href="tomconstants.htm">tomBoxStrikeTLBR</a></dt>
<dt><a href="tomconstants.htm">tomBoxStrikeBLTR</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomBrackets</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomAlignDefault</a></dt>
<dt><a href="tomconstants.htm">tomAlignCenter</a></dt>
<dt><a href="tomconstants.htm">tomAlignMatchAscentDescent</a></dt>
<dt><a href="tomconstants.htm">tomMathVariant</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomEquationArray</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomEqArrayLayoutWidth</a></dt>
<dt><a href="tomconstants.htm">tomEqArrayAlignMask</a></dt>
<dt><a href="tomconstants.htm">tomEqArrayAlignCenter</a></dt>
<dt><a href="tomconstants.htm">tomEqArrayAlignTopRow</a></dt>
<dt><a href="tomconstants.htm">tomEqArrayAlignBottomRow</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomMatrix</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomMatrixAlignMask</a></dt>
<dt><a href="tomconstants.htm">tomMatrixAlignCenter</a></dt>
<dt><a href="tomconstants.htm">tomMatrixAlignTopRow</a></dt>
<dt><a href="tomconstants.htm">tomMatrixAlignBottomRow</a></dt>
<dt><a href="tomconstants.htm">tomShowMatPlaceHldr</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomNary</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomLimitsDefault</a></dt>
<dt><a href="tomconstants.htm">tomLimitsUnderOver</a></dt>
<dt><a href="tomconstants.htm">tomLimitsSubSup</a></dt>
<dt><a href="tomconstants.htm">tomUpperLimitAsSuperScript</a></dt>
<dt><a href="tomconstants.htm">tomLimitsOpposite</a></dt>
<dt><a href="tomconstants.htm">tomShowLLimPlaceHldr</a></dt>
<dt><a href="tomconstants.htm">tomShowULimPlaceHldr</a></dt>
<dt><a href="tomconstants.htm">tomDontGrowWithContent</a></dt>
<dt><a href="tomconstants.htm">tomGrowWithContent</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomPhantom</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomPhantomShow</a></dt>
<dt><a href="tomconstants.htm">tomPhantomZeroWidth</a></dt>
<dt><a href="tomconstants.htm">tomPhantomZeroAscent</a></dt>
<dt><a href="tomconstants.htm">tomPhantomZeroDescent</a></dt>
<dt><a href="tomconstants.htm">tomPhantomTransparent
</a></dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomRadical</a></td>
<td><a href="tomconstants.htm">tomShowDegPlaceHldr</a></td>
</tr>
<tr>
<td><a href="objecttype.htm">tomSubSup</a></td>
<td><a href="tomconstants.htm">tomSubSupAlign</a></td>
</tr>
<tr>
<td><a href="objecttype.htm">tomStretchStack</a></td>
<td>
<dl>
<dt><a href="tomconstants.htm">tomStretchCharBelow</a></dt>
<dt><a href="tomconstants.htm">tomStretchCharAbove</a></dt>
<dt><a href="tomconstants.htm">tomStretchBaseBelow</a></dt>
<dt><a href="tomconstants.htm">tomStretchBaseAbove
</a></dt>
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
<td><a href="objecttype.htm">tomAccent</a></td>
<td>Accent (U+0300—U+36F, U+20D0—U+20EF)</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomBoxedFormula</a></td>
<td>U+25AD for rectangle enclosure</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomBrackets</a></td>
<td>Opening bracket. Default: U+0028.  </td>
</tr>
<tr>
<td><a href="objecttype.htm">tomBracketsWithSeps</a></td>
<td>Opening bracket with separators. Default: U+0028</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomEquationArray</a></td>
<td>U+2588</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomFraction</a></td>
<td>Normal built-up fraction: U+002F; small numeric fraction: U+2298</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomFunctionApply</a></td>
<td>U+2061</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomLeftSubSup</a></td>
<td>U+005E</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomLowerLimit</a></td>
<td>U+252C</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomMatrix</a></td>
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
<td><a href="objecttype.htm">tomNary</a></td>
<td>n-ary symbol</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomOpChar</a></td>
<td>Internal use for no-build operators</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomOverbar</a></td>
<td>U+00AF</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomPhantom</a></td>
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
<td><a href="objecttype.htm">tomRadical</a></td>
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
<td><a href="objecttype.htm">tomSlashedFraction</a></td>
<td>
<dl>
<dt>U+2044: skewed fraction</dt>
<dt>U+2215: built-up linear fraction
</dt>
</dl>
</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomStack</a></td>
<td>U+00A6

</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomStretchStack</a></td>
<td>Horizontal stretch character (see <a href="http://go.microsoft.com/fwlink/p/?linkid=124972">Unicode Technical Note 28</a> Appendix B for a list)</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomSubscript</a></td>
<td>U+005E




</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomSubSup</a></td>
<td>U+005E</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomSuperscript</a></td>
<td>U+005F</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomUnderbar</a></td>
<td>U+2581</td>
</tr>
<tr>
<td><a href="objecttype.htm">tomUpperLimit</a></td>
<td>U+2534</td>
</tr>
</table>
 




### -param pChar1 [out]

Type: <b>long*</b>

The closing <b>tomBrackets</b> character.  See <a href="http://go.microsoft.com/fwlink/p/?linkid=124972">Unicode Technical Note 28</a> Appendix B. Character Keywords and Properties for a list.


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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<a href="http://go.microsoft.com/fwlink/p/?linkid=124972">Unicode Technical Note 28</a> describes the alignment and character values in detail when the active end character is an inline object start delimiter. 

When that character is not a start delimiter, the character and column parameters are set to 0, the count is set to the 0-based argument index, and the other parameters are set according to the active-end character properties of the innermost inline object argument.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/56876a42-a972-4a19-a8f7-a5e37c0d77f0">ITextRange2::SetInlineObject</a>
 

 

