---
UID: NF:tom.ITextRange2.Linearize
title: ITextRange2::Linearize (tom.h)
description: Translates the built-up math, ruby, and other inline objects in this range to linearized form.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","Linearize method","ITextRange2.Linearize","ITextRange2::Linearize","Linearize","Linearize method [Windows Controls]","Linearize method [Windows Controls]","ITextRange2 interface","controls.itextrange2_linearize","tom/ITextRange2::Linearize","tomMathAlphabetics","tomMathBuildDownOutermost","tomMathBuildUpArgOrZone","tomMathRemoveOutermost","tomPlain","tomTeX"]
old-location: controls\itextrange2_linearize.htm
tech.root: Controls
ms.assetid: 9906547b-e31c-48a6-961e-0b7f5c0c0506
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],Linearize method, ITextRange2.Linearize, ITextRange2::Linearize, Linearize, Linearize method [Windows Controls], Linearize method [Windows Controls],ITextRange2 interface, controls.itextrange2_linearize, tom/ITextRange2::Linearize, tomMathAlphabetics, tomMathBuildDownOutermost, tomMathBuildUpArgOrZone, tomMathRemoveOutermost, tomPlain, tomTeX
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
 - ITextRange2::Linearize
 - tom/ITextRange2::Linearize
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
 - ITextRange2.Linearize
---

# ITextRange2::Linearize


## -description

Translates the built-up math, ruby, and other inline objects in this range to linearized form.

## -parameters

### -param Flags [in]

Type: <b>long</b>

A combination of the following flags.

<a id="tomMathAlphabetics"></a>
<a id="tommathalphabetics"></a>
<a id="TOMMATHALPHABETICS"></a>


#### tomMathAlphabetics

<a id="tomMathBuildDownOutermost"></a>
<a id="tommathbuilddownoutermost"></a>
<a id="TOMMATHBUILDDOWNOUTERMOST"></a>


#### tomMathBuildDownOutermost

<a id="tomMathBuildUpArgOrZone"></a>
<a id="tommathbuildupargorzone"></a>
<a id="TOMMATHBUILDUPARGORZONE"></a>


#### tomMathBuildUpArgOrZone

<a id="tomMathRemoveOutermost"></a>
<a id="tommathremoveoutermost"></a>
<a id="TOMMATHREMOVEOUTERMOST"></a>


#### tomMathRemoveOutermost

<a id="tomPlain"></a>
<a id="tomplain"></a>
<a id="TOMPLAIN"></a>


#### tomPlain

<a id="__tomTeX"></a>
<a id="__tomtex"></a>
<a id="__TOMTEX"></a>


#### tomTeX

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

If the linearization is successful, the originally selected range is replaced by the linearized version. 

If the <b>tomMathRemoveOutermost</b> or <b>tomMathBuildDownOutermost</b> build down mode is specified, the build down operation can be affected by the <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathChangeMask</a> values.

 The main purpose of these build-down modes is to facilitate transformations of the build-up math object as exposed by math context menus. 


For example, to convert a stacked fraction to a linear fraction as in
(a+b/c)/(u+x/y)→((a+b/c))⁄((u+x/y)),
parentheses must be inserted; otherwise, you get a transformation
that looks incorrect, as in (a+b/c)/(u+x/y)→(a+b/c)⁄(u+x/y),
even though internally the linear fraction still has the original numerator and denominator. 

The build-down process automatically inserts the parentheses, because the linear format for this case has parentheses, and the special change is made to replace the stacked-fraction operator U+002F by the linear fraction operator U+2215. Build up doesn't discard the parentheses for U+2215, but it does for U+002F.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-buildupmath">ITextRange2::BuildUpMath</a>