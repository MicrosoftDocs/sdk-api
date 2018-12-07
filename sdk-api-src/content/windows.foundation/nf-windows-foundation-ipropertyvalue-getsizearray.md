---
UID: NF:windows.foundation.IPropertyValue.GetSizeArray
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of Size values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getsizearray.htm
tech.root: WinRT
ms.assetid: f378c4d0-c3a2-4611-a471-0c77746602f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSizeArray, GetSizeArray method [Windows Runtime], GetSizeArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetSizeArray method, IPropertyValue.GetSizeArray, IPropertyValue.IPropertyValue, IPropertyValue::GetSizeArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetSizeArray, winrt.ipropertyvalue_getsizearray
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
 - IPropertyValue.GetSizeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of <a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a> values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a>**</b>

The array of <a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a> values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/8b9916e7-0a0d-44b1-8f8d-8307c145e57a">IPropertyValueStatics::CreateSizeArray</a>
 

 

