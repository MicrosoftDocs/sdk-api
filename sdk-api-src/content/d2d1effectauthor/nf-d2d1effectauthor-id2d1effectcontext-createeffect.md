---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateEffect
title: ID2D1EffectContext::CreateEffect
author: windows-sdk-content
description: Creates a Direct2D effect for the specified class ID.
old-location: direct2d\id2d1contextinternal_createeffect.htm
tech.root: direct2d
ms.assetid: BF903D96-F643-4C87-9191-A46B7CE3B12C
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateEffect, CreateEffect method [Direct2D], CreateEffect method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateEffect method, ID2D1EffectContext.CreateEffect, ID2D1EffectContext::CreateEffect, d2d1effectauthor/ID2D1EffectContext::CreateEffect, direct2d.id2d1contextinternal_createeffect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.CreateEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateEffect


## -description


Creates a Direct2D effect for the specified  class ID.
      This is the same as <a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a> so custom effects can create other effects and wrap them in a transform.


## -parameters




### -param effectId

Type: <b>REFCLSID</b>

The built-in or registered effect ID to create the effect. See <a href="https://msdn.microsoft.com/A76F6AB8-16E9-45C9-A768-5E4AA072D534">Built-in Effects</a> for a list of effect IDs.


### -param effect [out]

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>**</b>

When this method returns, contains the address of a pointer to the effect.


## -returns



Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.
                </td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
<tr>
<td>D3DERR_OUTOFVIDEOMEMORY</td>
<td>Direct3D does not have enough display memory to perform the operation.
                </td>
</tr>
<tr>
<td>D2DERR_EFFECT_IS_NOT_REGISTERED</td>
<td>The specified effect is not registered by the system.</td>
</tr>
</table>
 




## -remarks



The created effect does not reference count the DLL from which the effect was created. If the caller unregisters an effect while this effect is loaded, the resulting behavior is unpredictable.




## -see-also




<a href="https://msdn.microsoft.com/5f4c7248-9303-4451-92f1-4b230efd627a">D2D1_BLEND_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/1446BDA9-AD4C-472C-8F1D-82ABC1880E13">Effects</a>



<a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>



<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

