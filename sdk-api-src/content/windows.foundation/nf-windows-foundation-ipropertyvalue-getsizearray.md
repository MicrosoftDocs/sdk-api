---
UID: NF:windows.foundation.IPropertyValue.GetSizeArray
title: IPropertyValue::GetSizeArray (windows.foundation.h)
description: Gets the array of Size values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetSizeArray","GetSizeArray method [Windows Runtime]","GetSizeArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetSizeArray method","IPropertyValue.GetSizeArray","IPropertyValue.IPropertyValue","IPropertyValue::GetSizeArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetSizeArray","winrt.ipropertyvalue_getsizearray"]
old-location: winrt\ipropertyvalue_getsizearray.htm
tech.root: WinRT
ms.assetid: f378c4d0-c3a2-4611-a471-0c77746602f6
ms.date: 12/05/2018
ms.keywords: GetSizeArray, GetSizeArray method [Windows Runtime], GetSizeArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetSizeArray method, IPropertyValue.GetSizeArray, IPropertyValue.IPropertyValue, IPropertyValue::GetSizeArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetSizeArray, winrt.ipropertyvalue_getsizearray
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
 - IPropertyValue::GetSizeArray
 - windows.foundation/IPropertyValue::GetSizeArray
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
 - IPropertyValue.GetSizeArray
---

# IPropertyValue::GetSizeArray (windows.foundation.h)


## -description

Gets the array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a> values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a>**</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a> values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createsizearray">IPropertyValueStatics::CreateSizeArray</a>
