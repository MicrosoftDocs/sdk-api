---
UID: NF:d2d1_1.ID2D1Factory1.GetRegisteredEffects
title: ID2D1Factory1::GetRegisteredEffects (d2d1_1.h)
description: Returns the class IDs of the currently registered effects and global effects on this factory.
helpviewer_keywords: ["GetRegisteredEffects","GetRegisteredEffects method [Direct2D]","GetRegisteredEffects method [Direct2D]","ID2D1Factory1 interface","ID2D1Factory1 interface [Direct2D]","GetRegisteredEffects method","ID2D1Factory1.GetRegisteredEffects","ID2D1Factory1::GetRegisteredEffects","d2d1_1/ID2D1Factory1::GetRegisteredEffects","direct2d.id2d1factory1_getregisteredeffects"]
old-location: direct2d\id2d1factory1_getregisteredeffects.htm
tech.root: Direct2D
ms.assetid: c3363411-908f-4b02-b77e-ca563094f9a5
ms.date: 12/05/2018
ms.keywords: GetRegisteredEffects, GetRegisteredEffects method [Direct2D], GetRegisteredEffects method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],GetRegisteredEffects method, ID2D1Factory1.GetRegisteredEffects, ID2D1Factory1::GetRegisteredEffects, d2d1_1/ID2D1Factory1::GetRegisteredEffects, direct2d.id2d1factory1_getregisteredeffects
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory1::GetRegisteredEffects
 - d2d1_1/ID2D1Factory1::GetRegisteredEffects
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
 - ID2D1Factory1.GetRegisteredEffects
---

# ID2D1Factory1::GetRegisteredEffects


## -description

Returns the class IDs of the currently registered effects and global effects on this factory.

## -parameters

### -param effects [out]

Type: <b><a href="/windows/desktop/com/clsid">CLSID</a>*</b>

When this method returns, contains an array of effects. <b>NULL</b> if no effects are retrieved.

### -param effectsCount

Type: <b><a href="/windows/desktop/api/webservices/ns-webservices-ws_uint32_description">UINT32</a></b>

The capacity of the <i>effects</i> array.

### -param effectsReturned [out]

Type: <b><a href="/windows/desktop/api/webservices/ns-webservices-ws_uint32_description">UINT32</a>*</b>

When this method returns, contains the  number of effects copied into <i>effects</i>.

### -param effectsRegistered [out, optional]

Type: <b><a href="/windows/desktop/api/webservices/ns-webservices-ws_uint32_description">UINT32</a>*</b>

When this method returns, contains the number of effects currently registered in the system.

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
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</td>
<td><i>effectsRegistered</i> is larger than <i>effectCount</i>.</td>
</tr>
</table>

## -remarks

The set of class IDs will be atomically returned by the API. The set will not be interrupted by other threads registering or unregistering effects.

If <i>effectsRegistered</i> is larger than <i>effectCount</i>, the supplied array will still be filled to capacity with the current set of registered effects. This method returns the CLSIDs for all global effects and all effects registered to this factory.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory1::RegisterEffect</a>