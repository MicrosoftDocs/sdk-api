---
UID: NN:mileffects.IMILBitmapEffectRenderContextImpl
title: IMILBitmapEffectRenderContextImpl
author: windows-sdk-content
description: Exposes methods that define a IMILBitmapEffectRenderContext.
old-location: wibe\_wibe_imilbitmapeffectrendercontextimpl.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontextimpl\imilbitmapeffectrendercontextimpl.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: IMILBitmapEffectRenderContextImpl, IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects], IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectrendercontextimpl, mileffects/IMILBitmapEffectRenderContextImpl, wibe._wibe_imilbitmapeffectrendercontextimpl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.dll
api_name:
-	IMILBitmapEffectRenderContextImpl
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectRenderContextImpl interface


## -description


Exposes methods that define a <a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectRenderContextImpl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectRenderContextImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectRenderContextImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64030a15-477e-4f4e-8539-b36dc9af4970">GetOutputBounds</a>
</td>
<td align="left" width="63%">
Gets the output bounds of the render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2efce00a-93b8-477d-baae-1adb53cd369a">GetTransform</a>
</td>
<td align="left" width="63%">
Gets the matrix transform of the render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f344cf1-27db-4ef5-b1b5-c44bf6678e59">GetUseSoftwareRenderer</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether to use software rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57bb3729-95a5-4b77-9f89-f95fb7504586">UpdateOutputBounds</a>
</td>
<td align="left" width="63%">
Updates the output bounds with the given region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/592ea626-157e-4c9a-951b-b06dcd1c9f77">UpdateTransform</a>
</td>
<td align="left" width="63%">
Updates the output transform with the new matrix.

</td>
</tr>
</table> 

