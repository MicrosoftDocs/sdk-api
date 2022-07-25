---
UID: NF:windows.foundation.IPropertyValue.GetRectArray
title: IPropertyValue::GetRectArray (windows.foundation.h)
description: Gets the array of Rect values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetRectArray","GetRectArray method [Windows Runtime]","GetRectArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetRectArray method","IPropertyValue.GetRectArray","IPropertyValue.IPropertyValue","IPropertyValue::GetRectArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetRectArray","winrt.ipropertyvalue_getrectarray"]
old-location: winrt\ipropertyvalue_getrectarray.htm
tech.root: WinRT
ms.assetid: 7e1f39f6-0ccb-4841-ae5e-36adaf72a4ee
ms.date: 12/05/2018
ms.keywords: GetRectArray, GetRectArray method [Windows Runtime], GetRectArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetRectArray method, IPropertyValue.GetRectArray, IPropertyValue.IPropertyValue, IPropertyValue::GetRectArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetRectArray, winrt.ipropertyvalue_getrectarray
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
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
 - IPropertyValue::GetRectArray
 - windows.foundation/IPropertyValue::GetRectArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValue.GetRectArray
---

# IPropertyValue::GetRectArray (windows.foundation.h)


## -description

Gets the array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a>**</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createrectarray">IPropertyValueStatics::CreateRectArray</a>
