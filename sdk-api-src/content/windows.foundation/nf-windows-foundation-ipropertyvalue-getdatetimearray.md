---
UID: NF:windows.foundation.IPropertyValue.GetDateTimeArray
title: IPropertyValue::GetDateTimeArray (windows.foundation.h)
description: Gets the array of DateTime values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetDateTimeArray","GetDateTimeArray method [Windows Runtime]","GetDateTimeArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetDateTimeArray method","IPropertyValue.GetDateTimeArray","IPropertyValue.IPropertyValue","IPropertyValue::GetDateTimeArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetDateTimeArray","winrt.ipropertyvalue_getdatetimearray"]
old-location: winrt\ipropertyvalue_getdatetimearray.htm
tech.root: WinRT
ms.assetid: 76d18ef4-676c-4130-90e3-e74776e47f33
ms.date: 12/05/2018
ms.keywords: GetDateTimeArray, GetDateTimeArray method [Windows Runtime], GetDateTimeArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetDateTimeArray method, IPropertyValue.GetDateTimeArray, IPropertyValue.IPropertyValue, IPropertyValue::GetDateTimeArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetDateTimeArray, winrt.ipropertyvalue_getdatetimearray
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
 - IPropertyValue::GetDateTimeArray
 - windows.foundation/IPropertyValue::GetDateTimeArray
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
 - IPropertyValue.GetDateTimeArray
---

# IPropertyValue::GetDateTimeArray (windows.foundation.h)


## -description

Gets the array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a>**</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createdatetimearray">IPropertyValueStatics::CreateDateTimeArray</a>
