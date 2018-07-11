---
UID: NN:mileffects.IMILBitmapEffectRenderContext
title: IMILBitmapEffectRenderContext
author: windows-sdk-content
description: Exposes methods that define a IMILBitmapEffectRenderContext object.
old-location: wibe\_wibe_imilbitmapeffectrendercontext.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontext\imilbitmapeffectrendercontext.htm
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: IMILBitmapEffectRenderContext, IMILBitmapEffectRenderContext interface [WPF Bitmap Effects], IMILBitmapEffectRenderContext interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectrendercontext, mileffects/IMILBitmapEffectRenderContext, wibe._wibe_imilbitmapeffectrendercontext
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectRenderContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectRenderContext interface


## -description


Exposes methods that define a <b>IMILBitmapEffectRenderContext</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectRenderContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectRenderContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectRenderContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb620130-9fb4-425a-b3b2-95d6fd7cda6d">GetFinalTransform</a>
</td>
<td align="left" width="63%">
Gets the final <a href="https://msdn.microsoft.com/b75a27b4-2aac-42a0-b45e-c9fc84655513">MILMatrixF</a> transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f619b239-78a1-4038-b673-76911a85102b">GetOutputDPI</a>
</td>
<td align="left" width="63%">
Gets the output dpi.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cfb75d7-f953-44be-b735-d1de9812c98d">GetOutputPixelFormat</a>
</td>
<td align="left" width="63%">
Gets the output pixel format GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7b3ba37-41d1-481e-9b88-63b94525852b">SetInitialTransform</a>
</td>
<td align="left" width="63%">
Gets the initial <a href="https://msdn.microsoft.com/b75a27b4-2aac-42a0-b45e-c9fc84655513">MILMatrixF</a> transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b29a6ee-e8d1-4b4a-b579-66558f8d3e5a">SetOutputDPI</a>
</td>
<td align="left" width="63%">
Sets the output dpi.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eb16929-97b8-4c2d-9dfb-1998ac850c24">SetOutputPixelFormat</a>
</td>
<td align="left" width="63%">
Sets the output pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7172d853-55f3-49ff-bd17-b44468680598">SetRegionOfInterest</a>
</td>
<td align="left" width="63%">
Sets the region of interest for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/818f6078-28b1-494e-a7b4-31ffdd427288">SetUseSoftwareRenderer</a>
</td>
<td align="left" width="63%">
Sets a value to indicate whether to use software rendering.

</td>
</tr>
</table> 

