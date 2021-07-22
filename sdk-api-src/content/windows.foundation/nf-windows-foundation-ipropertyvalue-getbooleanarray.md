---
UID: NF:windows.foundation.IPropertyValue.GetBooleanArray
title: IPropertyValue::GetBooleanArray (windows.foundation.h)
description: Gets the array of 8-bit Boolean values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetBooleanArray","GetBooleanArray method [Windows Runtime]","GetBooleanArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetBooleanArray method","IPropertyValue.GetBooleanArray","IPropertyValue.IPropertyValue","IPropertyValue::GetBooleanArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetBooleanArray","winrt.ipropertyvalue_getbooleanarray"]
old-location: winrt\ipropertyvalue_getbooleanarray.htm
tech.root: WinRT
ms.assetid: 22ad7bab-87b1-41e8-ae65-1957e7c93b2e
ms.date: 12/05/2018
ms.keywords: GetBooleanArray, GetBooleanArray method [Windows Runtime], GetBooleanArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetBooleanArray method, IPropertyValue.GetBooleanArray, IPropertyValue.IPropertyValue, IPropertyValue::GetBooleanArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetBooleanArray, winrt.ipropertyvalue_getbooleanarray
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
 - IPropertyValue::GetBooleanArray
 - windows.foundation/IPropertyValue::GetBooleanArray
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
 - IPropertyValue.GetBooleanArray
---

# IPropertyValue::GetBooleanArray (windows.foundation.h)


## -description

Gets the array of 8-bit Boolean values that is stored in the current  <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b>boolean**</b>

The array of 8-bit Boolean values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createbooleanarray">CreateBooleanArray</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>
