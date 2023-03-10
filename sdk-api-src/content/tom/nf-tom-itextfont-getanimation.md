---
UID: NF:tom.ITextFont.GetAnimation
title: ITextFont::GetAnimation (tom.h)
description: Gets the animation type.
helpviewer_keywords: ["GetAnimation","GetAnimation method [Windows Controls]","GetAnimation method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetAnimation method","ITextFont.GetAnimation","ITextFont::GetAnimation","_win32_ITextFont_GetAnimation","_win32_ITextFont_GetAnimation_cpp","controls.ITextFont_GetAnimation","controls._win32_ITextFont_GetAnimation","tom/ITextFont::GetAnimation"]
old-location: controls\ITextFont_GetAnimation.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getanimation.htm
ms.date: 12/05/2018
ms.keywords: GetAnimation, GetAnimation method [Windows Controls], GetAnimation method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetAnimation method, ITextFont.GetAnimation, ITextFont::GetAnimation, _win32_ITextFont_GetAnimation, _win32_ITextFont_GetAnimation_cpp, controls.ITextFont_GetAnimation, controls._win32_ITextFont_GetAnimation, tom/ITextFont::GetAnimation
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
 - ITextFont::GetAnimation
 - tom/ITextFont::GetAnimation
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
 - ITextFont.GetAnimation
---

# ITextFont::GetAnimation


## -description

Gets the animation type.

## -parameters

### -param pValue

Type: <b>long*</b>

One of the following animation types. 
					

<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomNoAnimation</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomLasVegasLights</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomBlinkingBackground</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomSparkleText</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMarchingBlackAnts</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMarchingRedAnts</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomShimmer</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomWipeDown</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomWipeRight</a>

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
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setanimation">SetAnimation</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>