---
UID: NF:windows.foundation.IPropertyValue.GetPointArray
title: IPropertyValue::IPropertyValue (windows.foundation.h)
description: Gets the array of Point values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetPointArray","GetPointArray method [Windows Runtime]","GetPointArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetPointArray method","IPropertyValue.GetPointArray","IPropertyValue.IPropertyValue","IPropertyValue::GetPointArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetPointArray","winrt.ipropertyvalue_getpointarray"]
old-location: winrt\ipropertyvalue_getpointarray.htm
tech.root: WinRT
ms.assetid: 7df4ad4e-3ca6-4956-b907-02c2cb6e481b
ms.date: 12/05/2018
ms.keywords: GetPointArray, GetPointArray method [Windows Runtime], GetPointArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetPointArray method, IPropertyValue.GetPointArray, IPropertyValue.IPropertyValue, IPropertyValue::GetPointArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetPointArray, winrt.ipropertyvalue_getpointarray
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
 - IPropertyValue::GetPointArray
 - windows.foundation/IPropertyValue::GetPointArray
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
 - IPropertyValue.GetPointArray
---

# IPropertyValue::IPropertyValue


## -description

Gets the array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a>**</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> values.

The returned pointer must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createpointarray">IPropertyValueStatics::CreatePointArray</a>