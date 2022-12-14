---
UID: NF:windows.foundation.IPropertyValue.GetInt32Array
title: IPropertyValue::GetInt32Array (windows.foundation.h)
description: Gets the array of signed 32-bit integer values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetInt32Array","GetInt32Array method [Windows Runtime]","GetInt32Array method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetInt32Array method","IPropertyValue.GetInt32Array","IPropertyValue.IPropertyValue","IPropertyValue::GetInt32Array","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetInt32Array","winrt.ipropertyvalue_getint32array"]
old-location: winrt\ipropertyvalue_getint32array.htm
tech.root: WinRT
ms.assetid: ace88b14-951c-4482-a46d-12c4665c9450
ms.date: 12/05/2018
ms.keywords: GetInt32Array, GetInt32Array method [Windows Runtime], GetInt32Array method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetInt32Array method, IPropertyValue.GetInt32Array, IPropertyValue.IPropertyValue, IPropertyValue::GetInt32Array, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetInt32Array, winrt.ipropertyvalue_getint32array
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
 - IPropertyValue::GetInt32Array
 - windows.foundation/IPropertyValue::GetInt32Array
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
 - IPropertyValue.GetInt32Array
---

# IPropertyValue::GetInt32Array (windows.foundation.h)


## -description

Gets the array of signed 32-bit integer values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b>INT32**</b>

The array of signed 32-bit integer values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createint32array">IPropertyValueStatics::CreateInt32Array</a>
