---
UID: NF:windows.foundation.IPropertyValue.GetDoubleArray
title: IPropertyValue::IPropertyValue (windows.foundation.h)
author: windows-sdk-content
description: Gets the array of 64-bit floating point values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getdoublearray.htm
tech.root: WinRT
ms.assetid: 197a3626-e349-4027-913c-e8203dad4fc1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDoubleArray, GetDoubleArray method [Windows Runtime], GetDoubleArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetDoubleArray method, IPropertyValue.GetDoubleArray, IPropertyValue.IPropertyValue, IPropertyValue::GetDoubleArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetDoubleArray, winrt.ipropertyvalue_getdoublearray
ms.topic: method
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
 - IPropertyValue.GetDoubleArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of 64-bit floating point values that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b>DOUBLE**</b>

The array of 64-bit floating point values.

The returned pointer must be freed using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createdoublearray">IPropertyValueStatics::CreateDoubleArray</a>
 

 

