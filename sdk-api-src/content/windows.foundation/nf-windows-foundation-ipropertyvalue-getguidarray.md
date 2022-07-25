---
UID: NF:windows.foundation.IPropertyValue.GetGuidArray
title: IPropertyValue::GetGuidArray (windows.foundation.h)
description: Gets the array of Guid values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetGuidArray","GetGuidArray method [Windows Runtime]","GetGuidArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetGuidArray method","IPropertyValue.GetGuidArray","IPropertyValue.IPropertyValue","IPropertyValue::GetGuidArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetGuidArray","winrt.ipropertyvalue_getguidarray"]
old-location: winrt\ipropertyvalue_getguidarray.htm
tech.root: WinRT
ms.assetid: 83d19a18-3cd4-4343-8609-12e9a65b8e37
ms.date: 12/05/2018
ms.keywords: GetGuidArray, GetGuidArray method [Windows Runtime], GetGuidArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetGuidArray method, IPropertyValue.GetGuidArray, IPropertyValue.IPropertyValue, IPropertyValue::GetGuidArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetGuidArray, winrt.ipropertyvalue_getguidarray
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
 - IPropertyValue::GetGuidArray
 - windows.foundation/IPropertyValue::GetGuidArray
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
 - IPropertyValue.GetGuidArray
---

# IPropertyValue::GetGuidArray (windows.foundation.h)


## -description

Gets the array of <a href="/dotnet/api/system.guid">Guid</a> values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b>GUID**</b>

The array of <a href="/dotnet/api/system.guid">Guid</a> values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createguidarray">IPropertyValueStatics::CreateGuidArray</a>
