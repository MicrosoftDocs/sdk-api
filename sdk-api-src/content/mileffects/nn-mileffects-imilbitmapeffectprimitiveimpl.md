---
UID: NN:mileffects.IMILBitmapEffectPrimitiveImpl
title: IMILBitmapEffectPrimitiveImpl
author: windows-sdk-content
description: Exposes methods that report the state of a bitmap effect. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.
old-location: wibe\_wibe_imilbitmapeffectprimitiveimpl.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitiveimpl\imilbitmapeffectprimitiveimpl.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMILBitmapEffectPrimitiveImpl, IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects], IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectprimitiveimpl, mileffects/IMILBitmapEffectPrimitiveImpl, wibe._wibe_imilbitmapeffectprimitiveimpl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mileffects.h
req.include-header: 
req.redist: Microsoft .Net 3.0
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
 - Mileffects.h
api_name:
 - IMILBitmapEffectPrimitiveImpl
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitiveImpl interface


## -description


Exposes methods that report the state of a bitmap effect. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectPrimitiveImpl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectPrimitiveImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectPrimitiveImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04c21960-41bc-4bd3-8993-6dc9acc4510d">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether the effect needs to be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56bebc06-405b-4e5c-86c4-a96080297cd6">IsVolatile</a>
</td>
<td align="left" width="63%">
Determines whether the current effect is considered volatile. If an effect is volatile, the effects framework will not attempt to cache the effect's output.

</td>
</tr>
</table> 

