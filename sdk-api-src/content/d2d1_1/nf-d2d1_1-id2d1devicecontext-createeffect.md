---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateEffect
title: ID2D1DeviceContext::CreateEffect (d2d1_1.h)
description: Creates an effect for the specified class ID.
helpviewer_keywords: ["CreateEffect","CreateEffect method [Direct2D]","CreateEffect method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateEffect method","ID2D1DeviceContext.CreateEffect","ID2D1DeviceContext::CreateEffect","d2d1_1/ID2D1DeviceContext::CreateEffect","direct2d.id2d1devicecontext_createeffect"]
old-location: direct2d\id2d1devicecontext_createeffect.htm
tech.root: Direct2D
ms.assetid: dfe587f9-e92f-4367-a503-edd446a91cb8
ms.date: 12/05/2018
ms.keywords: CreateEffect, CreateEffect method [Direct2D], CreateEffect method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateEffect method, ID2D1DeviceContext.CreateEffect, ID2D1DeviceContext::CreateEffect, d2d1_1/ID2D1DeviceContext::CreateEffect, direct2d.id2d1devicecontext_createeffect
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::CreateEffect
 - d2d1_1/ID2D1DeviceContext::CreateEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.CreateEffect
---

# ID2D1DeviceContext::CreateEffect


## -description

Creates an effect for the specified class ID.

## -parameters

### -param effectId

Type: <b>REFCLSID</b>

The class ID of the effect to create. See <a href="/windows/desktop/Direct2D/built-in-effects">Built-in Effects</a> for a list of effect IDs.

### -param effect [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>**</b>

When this method returns, contains the address of a pointer to a new effect.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

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
<tr>
<td>E_NOTFOUND</td>
<td>Other possible HRESULT for an effect not being registered (like D2DERR_EFFECT_IS_NOT_REGISTERED).</td>
</tr>
<tr>
<td>D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES </td>
<td>The effect requires capabilities not supported by the D2D device.</td>
</tr>
</table>

## -remarks

If the  created effect is a custom effect that is implemented in a DLL, this doesn't increment the reference count for that DLL. 
        If the application deletes an effect while that effect is loaded, the resulting behavior is unpredictable.

## -see-also

<a href="/windows/desktop/Direct2D/effects-overview">Effects</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory1::RegisterEffect</a>
