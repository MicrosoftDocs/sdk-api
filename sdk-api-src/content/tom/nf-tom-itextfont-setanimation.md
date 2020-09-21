---
UID: NF:tom.ITextFont.SetAnimation
title: ITextFont::SetAnimation (tom.h)
description: Sets the animation type.
helpviewer_keywords: ["ITextFont interface [Windows Controls]","SetAnimation method","ITextFont.SetAnimation","ITextFont::SetAnimation","SetAnimation","SetAnimation method [Windows Controls]","SetAnimation method [Windows Controls]","ITextFont interface","_win32_ITextFont_SetAnimation","_win32_ITextFont_SetAnimation_cpp","controls.ITextFont_SetAnimation","controls._win32_ITextFont_SetAnimation","tom/ITextFont::SetAnimation"]
old-location: controls\ITextFont_SetAnimation.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setanimation.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],SetAnimation method, ITextFont.SetAnimation, ITextFont::SetAnimation, SetAnimation, SetAnimation method [Windows Controls], SetAnimation method [Windows Controls],ITextFont interface, _win32_ITextFont_SetAnimation, _win32_ITextFont_SetAnimation_cpp, controls.ITextFont_SetAnimation, controls._win32_ITextFont_SetAnimation, tom/ITextFont::SetAnimation
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
 - ITextFont::SetAnimation
 - tom/ITextFont::SetAnimation
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
 - ITextFont.SetAnimation
---

# ITextFont::SetAnimation


## -description

Sets the animation type.

## -parameters

### -param Value [in]

Type: <b>long</b>

The animation type. It can be one of the following values.

<table class="clsStd">
<tr>
<th>Animation type</th>
<th>Value</th>
</tr>
<tr>
<td><b>tomNoAnimation</b></td>
<td>0</td>
</tr>
<tr>
<td><b>tomLasVegasLights</b></td>
<td>1</td>
</tr>
<tr>
<td><b>tomBlinkingBackground</b></td>
<td>2</td>
</tr>
<tr>
<td><b>tomSparkleText</b></td>
<td>3</td>
</tr>
<tr>
<td><b>tomMarchingBlackAnts</b></td>
<td>4</td>
</tr>
<tr>
<td><b>tomMarchingRedAnts</b></td>
<td>5</td>
</tr>
<tr>
<td><b>tomShimmer</b></td>
<td>6</td>
</tr>
<tr>
<td><b>tomWipeDown</b></td>
<td>7</td>
</tr>
<tr>
<td><b>tomWipeRight</b></td>
<td>8</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-getanimation">GetAnimation</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>