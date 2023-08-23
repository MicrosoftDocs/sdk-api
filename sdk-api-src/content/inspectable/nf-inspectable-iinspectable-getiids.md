---
UID: NF:inspectable.IInspectable.GetIids
title: IInspectable::GetIids (inspectable.h)
description: Gets the interfaces that are implemented by the current Windows Runtime class.
helpviewer_keywords: ["GetIids","GetIids method [Windows Runtime]","GetIids method [Windows Runtime]","IInputPaneInterop interface","GetIids method [Windows Runtime]","IInspectable interface","IInputPaneInterop interface [Windows Runtime]","GetIids method","IInputPaneInterop::GetIids","IInspectable interface [Windows Runtime]","GetIids method","IInspectable.GetIids","IInspectable::GetIids","inspectable/IInputPaneInterop::GetIids","inspectable/IInspectable::GetIids","winrt.iinspectable_getiids"]
old-location: winrt\iinspectable_getiids.htm
tech.root: WinRT
ms.assetid: 560094E6-3ED2-4BF3-85C7-07736ECBACC8
ms.date: 12/05/2018
ms.keywords: GetIids, GetIids method [Windows Runtime], GetIids method [Windows Runtime],IInputPaneInterop interface, GetIids method [Windows Runtime],IInspectable interface, IInputPaneInterop interface [Windows Runtime],GetIids method, IInputPaneInterop::GetIids, IInspectable interface [Windows Runtime],GetIids method, IInspectable.GetIids, IInspectable::GetIids, inspectable/IInputPaneInterop::GetIids, inspectable/IInspectable::GetIids, winrt.iinspectable_getiids
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInspectable::GetIids
 - inspectable/IInspectable::GetIids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inspectable.h
api_name:
 - IInspectable.GetIids
 - IInputPaneInterop.GetIids
---

## -description

Gets the interfaces that are implemented by the current Windows Runtime class.

## -parameters

### -param iidCount [out]

Type: <b>ULONG*</b>

The number of interfaces that are implemented by the current Windows Runtime object, excluding the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> implementations.

### -param iids [out]

Type: <b>IID**</b>

A pointer to an array that contains an IID for each interface implemented by the current Windows Runtime object. The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interfaces are excluded.

## -returns

Type: <b>HRESULT</b>

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The IID array was allocated and saved in <i>iids</i> successfully.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate <i>iids</i>.

</td>
</tr>
</table>

## -remarks

Use the <b>GetIids</b> method to discover the interfaces that are implemented by a Windows Runtime object.

A <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call on any IID in the <i>iids</i> array must succeed.

The caller is responsible for freeing the IID array by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop">IInputPaneInterop</a>

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>

[winrt::get_interfaces](/uwp/cpp-ref-for-winrt/get-interfaces)
