---
UID: NF:d2d1_1.D2D1CreateDeviceContext
title: D2D1CreateDeviceContext function (d2d1_1.h)
description: Creates a new Direct2D device context associated with a DXGI surface.
helpviewer_keywords: ["D2D1CreateDeviceContext","D2D1CreateDeviceContext function [Direct2D]","d2d1_1/D2D1CreateDeviceContext","direct2d.d2d1createdevicecontext"]
old-location: direct2d\d2d1createdevicecontext.htm
tech.root: Direct2D
ms.assetid: 0e56d057-20a5-47b7-aec9-63c8e31f349b
ms.date: 12/05/2018
ms.keywords: D2D1CreateDeviceContext, D2D1CreateDeviceContext function [Direct2D], d2d1_1/D2D1CreateDeviceContext, direct2d.d2d1createdevicecontext
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
req.lib: d2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1CreateDeviceContext
 - d2d1_1/D2D1CreateDeviceContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d2d1.dll
api_name:
 - D2D1CreateDeviceContext
---

# D2D1CreateDeviceContext function


## -description

Creates a new Direct2D device context associated with a DXGI surface.

## -parameters

### -param dxgiSurface [in]

The DXGI surface the Direct2D device context is associated with.

### -param creationProperties [in, optional]

The properties to apply to the Direct2D device context.

### -param d2dDeviceContext [out]

When this function returns, contains the address of a pointer to a Direct2D device context.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>

## -remarks

This function will also create a new <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a> that can be retrieved through <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1resource-getfactory">ID2D1Resource::GetFactory</a>.

This function will also create a new <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> that can be retrieved through <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getdevice">ID2D1DeviceContext::GetDevice</a>.

The DXGI device will be specified implicitly through <i>dxgiSurface</i>.

If <i>creationProperties</i> are not specified, the Direct2D device will inherit its threading mode from the DXGI device implied by <i>dxgiSurface</i> and debug tracing will not be enabled.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice">D2D1CreateDevice</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext">D2D1CreateDeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_creation_properties">D2D1_CREATION_PROPERTIES</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1resource-getfactory">ID2D1Resource::GetFactory</a>