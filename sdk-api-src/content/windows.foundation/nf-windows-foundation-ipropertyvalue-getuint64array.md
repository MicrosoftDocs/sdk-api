---
UID: NF:windows.foundation.IPropertyValue.GetUInt64Array
title: IPropertyValue::GetUInt64Array (windows.foundation.h)
description: Gets the array of unsigned 64-bit integer values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetUInt64Array","GetUInt64Array method [Windows Runtime]","GetUInt64Array method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetUInt64Array method","IPropertyValue.GetUInt64Array","IPropertyValue.IPropertyValue","IPropertyValue::GetUInt64Array","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetUInt64Array","winrt.ipropertyvalue_getuint64array"]
old-location: winrt\ipropertyvalue_getuint64array.htm
tech.root: WinRT
ms.assetid: 2981b2dc-d3ec-4886-a191-4dade13c7f32
ms.date: 12/05/2018
ms.keywords: GetUInt64Array, GetUInt64Array method [Windows Runtime], GetUInt64Array method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetUInt64Array method, IPropertyValue.GetUInt64Array, IPropertyValue.IPropertyValue, IPropertyValue::GetUInt64Array, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetUInt64Array, winrt.ipropertyvalue_getuint64array
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
 - IPropertyValue::GetUInt64Array
 - windows.foundation/IPropertyValue::GetUInt64Array
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
 - IPropertyValue.GetUInt64Array
---

# IPropertyValue::GetUInt64Array (windows.foundation.h)


## -description

Gets the array of unsigned 64-bit integer values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b>UINT64**</b>

The array of unsigned 64-bit integer values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createuint64array">IPropertyValueStatics::CreateUInt64Array</a>
