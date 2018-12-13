---
UID: NF:windows.foundation.IPropertyValue.GetStringArray
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of string values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getstringarray.htm
tech.root: WinRT
ms.assetid: d256b888-efa0-470e-b54f-5cf8ddd6fd8a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStringArray, GetStringArray method [Windows Runtime], GetStringArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetStringArray method, IPropertyValue.GetStringArray, IPropertyValue.IPropertyValue, IPropertyValue::GetStringArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetStringArray, winrt.ipropertyvalue_getstringarray
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
 - IPropertyValue.GetStringArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of string values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>**</b>

The array of string values.

The returned strings must be freed using <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>. The returned objects must be released using <b>IUnknown::Release</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/b9741a88-4585-4eda-b21d-5af0e541ef48">IPropertyValueStatics::CreateStringArray</a>
 

 

