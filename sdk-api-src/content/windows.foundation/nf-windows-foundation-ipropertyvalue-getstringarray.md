---
UID: NF:windows.foundation.IPropertyValue.GetStringArray
title: IPropertyValue::GetStringArray (windows.foundation.h)
description: Gets the array of string values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetStringArray","GetStringArray method [Windows Runtime]","GetStringArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetStringArray method","IPropertyValue.GetStringArray","IPropertyValue.IPropertyValue","IPropertyValue::GetStringArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetStringArray","winrt.ipropertyvalue_getstringarray"]
old-location: winrt\ipropertyvalue_getstringarray.htm
tech.root: WinRT
ms.assetid: d256b888-efa0-470e-b54f-5cf8ddd6fd8a
ms.date: 12/05/2018
ms.keywords: GetStringArray, GetStringArray method [Windows Runtime], GetStringArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetStringArray method, IPropertyValue.GetStringArray, IPropertyValue.IPropertyValue, IPropertyValue::GetStringArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetStringArray, winrt.ipropertyvalue_getstringarray
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
 - IPropertyValue::GetStringArray
 - windows.foundation/IPropertyValue::GetStringArray
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
 - IPropertyValue.GetStringArray
---

# IPropertyValue::GetStringArray (windows.foundation.h)


## -description

Gets the array of string values that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.

### -param value [out]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>**</b>

The array of string values.

The returned strings must be freed using <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>. The returned objects must be released using <b>IUnknown::Release</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createstringarray">IPropertyValueStatics::CreateStringArray</a>
