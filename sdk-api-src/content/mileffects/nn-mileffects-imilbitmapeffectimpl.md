---
UID: NN:mileffects.IMILBitmapEffectImpl
title: IMILBitmapEffectImpl
author: windows-sdk-content
description: Exposes methods that define an an out IMILBitmapEffect object.
old-location: wibe\_wibe_imilbitmapeffectimpl.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\imilbitmapeffectimpl.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMILBitmapEffectImpl, IMILBitmapEffectImpl interface [WPF Bitmap Effects], IMILBitmapEffectImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectimpl, mileffects/IMILBitmapEffectImpl, wibe._wibe_imilbitmapeffectimpl
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


Exposes methods that define an an out <a href="https://msdn.microsoft.com/en-us/library/ms735317(v=VS.85).aspx">IMILBitmapEffect</a> object.


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
<a href="https://msdn.microsoft.com/en-us/library/ms735275(v=VS.85).aspx">GetInputBitmapSource</a>
</td>
<td align="left" width="63%">
Gets the input bitmap source of the effect of the given render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735276(v=VS.85).aspx">GetInputSource</a>
</td>
<td align="left" width="63%">
Retrieves the input <a href="https://msdn.microsoft.com/en-us/library/Ee690171(v=VS.85).aspx">IWICBitmapSource Interface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735277(v=VS.85).aspx">GetInputSourceBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of the input source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735278(v=VS.85).aspx">GetOutputBitmapSource</a>
</td>
<td align="left" width="63%">
Gets the output bitmap source of the effect of the given render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735280(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the effect with the given object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735282(v=VS.85).aspx">IsInPlaceModificationAllowed</a>
</td>
<td align="left" width="63%">
Determines whether the effect allows in-place modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735283(v=VS.85).aspx">SetParentEffect</a>
</td>
<td align="left" width="63%">
Sets the parent of the effect.

</td>
</tr>
</table> 


## -remarks



This interface must be implemented if a custom effect also exposes <a href="https://msdn.microsoft.com/en-us/library/ms735317(v=VS.85).aspx">IMILBitmapEffect</a>.



