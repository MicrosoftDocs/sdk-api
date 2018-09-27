---
UID: NF:windows.foundation.IPropertyValue.GetRectArray
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of Rect values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getrectarray.htm
tech.root: WinRT
ms.assetid: 7e1f39f6-0ccb-4841-ae5e-36adaf72a4ee
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRectArray, GetRectArray method [Windows Runtime], GetRectArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetRectArray method, IPropertyValue.GetRectArray, IPropertyValue.IPropertyValue, IPropertyValue::GetRectArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetRectArray, winrt.ipropertyvalue_getrectarray
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
 - IPropertyValue.GetRectArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> values that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize

TBD


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a>**</b>

The array of <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - length [out]

Type: <b>UINT32*</b>

The number of values in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/945f9c0a-22fe-42f6-b29b-3260607345f7">IPropertyValueStatics::CreateRectArray</a>
 

 

