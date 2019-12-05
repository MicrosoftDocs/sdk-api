---
UID: NF:windows.foundation.IPropertyValue.GetChar16Array
title: IPropertyValue::IPropertyValue (windows.foundation.h)
description: Gets the the array of Unicode characters that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getchar16array.htm
tech.root: WinRT
ms.assetid: b0649a8b-8060-4e0f-956e-879fe4185b11
ms.date: 12/05/2018
ms.keywords: GetChar16Array, GetChar16Array method [Windows Runtime], GetChar16Array method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetChar16Array method, IPropertyValue.GetChar16Array, IPropertyValue.IPropertyValue, IPropertyValue::GetChar16Array, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetChar16Array, winrt.ipropertyvalue_getchar16array
ms.topic: method
f1_keywords:
- windows.foundation/IPropertyValue.GetChar16Array
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windows.Foundation.h
api_name:
- IPropertyValue.GetChar16Array
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValue::IPropertyValue


## -description


Gets the the array of Unicode characters that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of Unicode characters in the array.


### -param value [out]

Type: <b>WCHAR**</b>

The array of Unicode characters.

The returned pointer must be freed using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createchar16array">IPropertyValueStatics::CreateChar16Array</a>
 

 

