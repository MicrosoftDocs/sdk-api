---
UID: NF:windows.foundation.IPropertyValue.GetSingleArray
title: IPropertyValue::GetSingleArray (windows.foundation.h)
description: Gets the array of 32-bit floating point values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetSingleArray","GetSingleArray method [Windows Runtime]","GetSingleArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetSingleArray method","IPropertyValue.GetSingleArray","IPropertyValue.IPropertyValue","IPropertyValue::GetSingleArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetSingleArray","winrt.ipropertyvalue_getsinglearray"]
old-location: winrt\ipropertyvalue_getsinglearray.htm
tech.root: WinRT
ms.assetid: f4286901-92b2-4707-9da7-bb7abf83bb87
ms.date: 12/05/2018
ms.keywords: GetSingleArray, GetSingleArray method [Windows Runtime], GetSingleArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetSingleArray method, IPropertyValue.GetSingleArray, IPropertyValue.IPropertyValue, IPropertyValue::GetSingleArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetSingleArray, winrt.ipropertyvalue_getsinglearray
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
 - IPropertyValue::GetSingleArray
 - windows.foundation/IPropertyValue::GetSingleArray
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
 - IPropertyValue.GetSingleArray
---

# IPropertyValue::GetSingleArray (windows.foundation.h)


## -description

Gets the array of 32-bit floating point values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b>FLOAT**</b>

The array of 32-bit floating point values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createsinglearray">IPropertyValueStatics::CreateSingleArray</a>
