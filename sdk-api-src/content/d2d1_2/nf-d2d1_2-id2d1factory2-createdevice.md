---
UID: NF:d2d1_2.ID2D1Factory2.CreateDevice
title: ID2D1Factory2::CreateDevice (d2d1_2.h)
description: Creates an ID2D1Device1 object.
helpviewer_keywords: ["CreateDevice","CreateDevice method [Direct2D]","CreateDevice method [Direct2D]","ID2D1Factory2 interface","ID2D1Factory2 interface [Direct2D]","CreateDevice method","ID2D1Factory2.CreateDevice","ID2D1Factory2::CreateDevice","d2d1_2/ID2D1Factory2::CreateDevice","direct2d.id2d1factory2_createdevice"]
old-location: direct2d\id2d1factory2_createdevice.htm
tech.root: Direct2D
ms.assetid: 1C7B5FE0-23DB-417F-8614-53848D61A054
ms.date: 12/05/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory2 interface, ID2D1Factory2 interface [Direct2D],CreateDevice method, ID2D1Factory2.CreateDevice, ID2D1Factory2::CreateDevice, d2d1_2/ID2D1Factory2::CreateDevice, direct2d.id2d1factory2_createdevice
req.header: d2d1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ID2D1Factory2::CreateDevice
 - d2d1_2/ID2D1Factory2::CreateDevice
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
 - ID2D1Factory2.CreateDevice
---

# ID2D1Factory2::CreateDevice


## -description

Creates an <a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a> object.

## -parameters

### -param dxgiDevice [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>*</b>

The <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> object used when creating  the <a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a>.

### -param d2dDevice1 [out]

Type: <b><a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a>**</b>

The requested <a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a> object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

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
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
<tr>
<td>D3DERR_OUTOFVIDEOMEMORY</td>
<td>Direct3D does not have enough display memory to perform the operation.</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device defines a resource domain in which a set of Direct2D objects and Direct2D device contexts can be used together.  Each call to <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice">CreateDevice</a> returns a unique <a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a> object, even if you pass the same <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> multiple times.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>



<a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getdevice">ID2D1DeviceContext::GetDevice</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>



<a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1factory2">ID2D1Factory2</a>