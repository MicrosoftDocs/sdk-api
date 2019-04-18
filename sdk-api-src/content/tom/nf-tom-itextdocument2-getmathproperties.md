---
UID: NF:tom.ITextDocument2.GetMathProperties
title: ITextDocument2::GetMathProperties (tom.h)
author: windows-sdk-content
description: Gets the math properties for the document.
old-location: controls\itextdocument2_getmathproperties.htm
tech.root: Controls
ms.assetid: 7686d0d6-5f49-4ab6-8a9e-1e53447ffe27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMathProperties, GetMathProperties method [Windows Controls], GetMathProperties method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetMathProperties method, ITextDocument2.GetMathProperties, ITextDocument2::GetMathProperties, controls.itextdocument2_getmathproperties, tom/ITextDocument2::GetMathProperties, tomMathBrkBinAfter, tomMathBrkBinBefore, tomMathBrkBinDup, tomMathBrkBinMask, tomMathBrkBinSubMM, tomMathBrkBinSubMP, tomMathBrkBinSubMask, tomMathBrkBinSubPM, tomMathDispAlignCenter, tomMathDispAlignLeft, tomMathDispAlignMask, tomMathDispAlignRight, tomMathDispDef, tomMathDispFracTeX, tomMathDispIntUnderOver, tomMathDispNaryGrow, tomMathDispNarySubSup, tomMathDocDiffItalic, tomMathDocDiffMask, tomMathDocDiffOpenItalic, tomMathDocDiffUpright, tomMathDocEmptyArgAlways, tomMathDocEmptyArgAuto, tomMathDocEmptyArgMask, tomMathDocEmptyArgNever, tomMathDocSbSpOpUnchanged, tomMathEnableRtl
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetMathProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument2::GetMathProperties


## -description


Gets the math properties for the document.


## -parameters




### -param pOptions [out]

Type: <b>long*</b>

A combination of the following math properties. 

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomMathDispAlignMask"></a><a id="tommathdispalignmask"></a><a id="TOMMATHDISPALIGNMASK"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispAlignMask</a></b></dt>
</dl>
</td>
<td width="60%">
Display-mode alignment mask.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispAlignCenter"></a><a id="tommathdispaligncenter"></a><a id="TOMMATHDISPALIGNCENTER"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispAlignCenter</a></b></dt>
</dl>
</td>
<td width="60%">
Center (default) alignment.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispAlignLeft"></a><a id="tommathdispalignleft"></a><a id="TOMMATHDISPALIGNLEFT"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispAlignLeft</a></b></dt>
</dl>
</td>
<td width="60%">
Left alignment.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispAlignRight"></a><a id="tommathdispalignright"></a><a id="TOMMATHDISPALIGNRIGHT"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispAlignRight</a></b></dt>
</dl>
</td>
<td width="60%">
Right alignment.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispIntUnderOver"></a><a id="tommathdispintunderover"></a><a id="TOMMATHDISPINTUNDEROVER"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispIntUnderOver</a></b></dt>
</dl>
</td>
<td width="60%">
Display-mode integral limits location.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispFracTeX"></a><a id="tommathdispfractex"></a><a id="TOMMATHDISPFRACTEX"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispFracTeX</a></b></dt>
</dl>
</td>
<td width="60%">
Display-mode nested fraction script size.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispNaryGrow"></a><a id="tommathdispnarygrow"></a><a id="TOMMATHDISPNARYGROW"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispNaryGrow</a></b></dt>
</dl>
</td>
<td width="60%">
Math-paragraph n-ary grow.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocEmptyArgMask"></a><a id="tommathdocemptyargmask"></a><a id="TOMMATHDOCEMPTYARGMASK"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocEmptyArgMask</a></b></dt>
</dl>
</td>
<td width="60%">
Empty arguments display mask.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocEmptyArgAuto_"></a><a id="tommathdocemptyargauto_"></a><a id="TOMMATHDOCEMPTYARGAUTO_"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocEmptyArgAuto </a></b></dt>
</dl>
</td>
<td width="60%">
Automatically use a dotted square to denote empty arguments, if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocEmptyArgAlways"></a><a id="tommathdocemptyargalways"></a><a id="TOMMATHDOCEMPTYARGALWAYS"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocEmptyArgAlways</a></b></dt>
</dl>
</td>
<td width="60%">
Always use a dotted square to denote empty arguments..

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocEmptyArgNever"></a><a id="tommathdocemptyargnever"></a><a id="TOMMATHDOCEMPTYARGNEVER"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocEmptyArgNever</a></b></dt>
</dl>
</td>
<td width="60%">
Don't denote empty arguments. 

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocSbSpOpUnchanged"></a><a id="tommathdocsbspopunchanged"></a><a id="TOMMATHDOCSBSPOPUNCHANGED"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocSbSpOpUnchanged</a></b></dt>
</dl>
</td>
<td width="60%">
Display the underscore (_) and caret (^) as themselves.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocDiffMask"></a><a id="tommathdocdiffmask"></a><a id="TOMMATHDOCDIFFMASK"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocDiffMask</a></b></dt>
</dl>
</td>
<td width="60%">
Style mask for the <b>tomMathDocDiffUpright</b>, <b>tomMathDocDiffItalic</b>, <b>tomMathDocDiffOpenItalic </b>options.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocDiffItalic"></a><a id="tommathdocdiffitalic"></a><a id="TOMMATHDOCDIFFITALIC"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocDiffItalic</a></b></dt>
</dl>
</td>
<td width="60%">
Use italic (default) for math differentials.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocDiffUpright"></a><a id="tommathdocdiffupright"></a><a id="TOMMATHDOCDIFFUPRIGHT"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocDiffUpright</a></b></dt>
</dl>
</td>
<td width="60%">
Use an upright font for math differentials.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDocDiffOpenItalic"></a><a id="tommathdocdiffopenitalic"></a><a id="TOMMATHDOCDIFFOPENITALIC"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDocDiffOpenItalic</a></b></dt>
</dl>
</td>
<td width="60%">
Use open italic (default) for math differentials.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispNarySubSup"></a><a id="tommathdispnarysubsup"></a><a id="TOMMATHDISPNARYSUBSUP"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispNarySubSup</a></b></dt>
</dl>
</td>
<td width="60%">
Math-paragraph non-integral n-ary limits location.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathDispDef"></a><a id="tommathdispdef"></a><a id="TOMMATHDISPDEF"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathDispDef</a></b></dt>
</dl>
</td>
<td width="60%">
Math-paragraph spacing defaults.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathEnableRtl"></a><a id="tommathenablertl"></a><a id="TOMMATHENABLERTL"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathEnableRtl</a></b></dt>
</dl>
</td>
<td width="60%">
Enable right-to-left (RTL) math zones in RTL paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinMask"></a><a id="tommathbrkbinmask"></a><a id="TOMMATHBRKBINMASK"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinMask</a></b></dt>
</dl>
</td>
<td width="60%">
Equation line break mask.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinBefore"></a><a id="tommathbrkbinbefore"></a><a id="TOMMATHBRKBINBEFORE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinBefore</a></b></dt>
</dl>
</td>
<td width="60%">
Break before binary/relational operator.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinAfter"></a><a id="tommathbrkbinafter"></a><a id="TOMMATHBRKBINAFTER"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinAfter</a></b></dt>
</dl>
</td>
<td width="60%">
Break after binary/relational operator.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinDup"></a><a id="tommathbrkbindup"></a><a id="TOMMATHBRKBINDUP"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinDup</a></b></dt>
</dl>
</td>
<td width="60%">
Duplicate binary/relational before/after.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinSubMask"></a><a id="tommathbrkbinsubmask"></a><a id="TOMMATHBRKBINSUBMASK"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinSubMask</a></b></dt>
</dl>
</td>
<td width="60%">
Duplicate mask for minus operator.

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinSubMM"></a><a id="tommathbrkbinsubmm"></a><a id="TOMMATHBRKBINSUBMM"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinSubMM</a></b></dt>
</dl>
</td>
<td width="60%">
- - (minus on both lines).

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinSubPM"></a><a id="tommathbrkbinsubpm"></a><a id="TOMMATHBRKBINSUBPM"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinSubPM</a></b></dt>
</dl>
</td>
<td width="60%">
+ -

</td>
</tr>
<tr>
<td width="40%"><a id="tomMathBrkBinSubMP"></a><a id="tommathbrkbinsubmp"></a><a id="TOMMATHBRKBINSUBMP"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomMathBrkBinSubMP</a></b></dt>
</dl>
</td>
<td width="60%">
- +

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/30775a51-0e63-453e-ac94-39d4510002f0">  ITextDocument2::GetProperty</a>



<a href="https://msdn.microsoft.com/a688354b-b231-44fc-9cfb-32c8e8b1361f">  ITextDocument2::SetMathProperties</a>
 

 

