---
UID: NF:windows.foundation.IPropertyValue.GetInt64Array
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of signed 64-bit integer values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getint64array.htm
tech.root: WinRT
ms.assetid: 8bc05817-e9d4-427a-883d-495faf5d0ab0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetInt64Array, GetInt64Array method [Windows Runtime], GetInt64Array method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetInt64Array method, IPropertyValue.GetInt64Array, IPropertyValue.IPropertyValue, IPropertyValue::GetInt64Array, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetInt64Array, winrt.ipropertyvalue_getint64array
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPropertyValue.GetInt64Array
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.foundation.h
: 
- IPropertyValue.GetInt64Array
: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of signed 64-bit integer values that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize

TBD


### -param value [out]

Type: <b>INT64**</b>

The array of signed 64-bit integer values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - length [out]

Type: <b>UINT32*</b>

The number of values in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/c226a049-e8e5-4283-a8c4-102beed08b23">IPropertyValueStatics::CreateInt64Array</a>
 

 

