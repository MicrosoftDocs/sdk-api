---
UID: NN:mileffects.IMILBitmapEffectImpl
title: IMILBitmapEffectImpl
author: windows-sdk-content
description: Exposes methods that define an an out IMILBitmapEffect object.
old-location: wibe\_wibe_imilbitmapeffectimpl.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\imilbitmapeffectimpl.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMILBitmapEffectImpl, IMILBitmapEffectImpl interface [WPF Bitmap Effects], IMILBitmapEffectImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectimpl, mileffects/IMILBitmapEffectImpl, wibe._wibe_imilbitmapeffectimpl
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
req.lib: 
req.dll: Mileffects.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectImpl
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectImpl interface


## -description


Exposes methods that define an an out <a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectImpl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89c25f96-e328-48eb-a169-3e946e02f1a0">GetInputBitmapSource</a>
</td>
<td align="left" width="63%">
Gets the input bitmap source of the effect of the given render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f82a879c-a764-4a28-a9db-7784e2966837">GetInputSource</a>
</td>
<td align="left" width="63%">
Retrieves the input <a href="_wic_codec_iwicbitmapsource">IWICBitmapSource Interface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c52c6ed-fdbb-41fa-a7b9-f916240c4647">GetInputSourceBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of the input source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7b82680-97da-430f-83a6-4d61d30060e1">GetOutputBitmapSource</a>
</td>
<td align="left" width="63%">
Gets the output bitmap source of the effect of the given render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b5fd4e-cab0-4d64-a650-ca8451082975">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the effect with the given object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03217107-6200-45cc-8101-eb912b3f4722">IsInPlaceModificationAllowed</a>
</td>
<td align="left" width="63%">
Determines whether the effect allows in-place modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57b0f1e3-5feb-4407-a0d5-ec547619d4ec">SetParentEffect</a>
</td>
<td align="left" width="63%">
Sets the parent of the effect.

</td>
</tr>
</table> 


## -remarks



This interface must be implemented if a custom effect also exposes <a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a>.



