---
UID: NF:windows.foundation.IPropertyValue.GetBooleanArray
title: IPropertyValue::IPropertyValue (windows.foundation.h)
author: windows-sdk-content
description: Gets the array of 8-bit Boolean values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getbooleanarray.htm
tech.root: WinRT
ms.assetid: 22ad7bab-87b1-41e8-ae65-1957e7c93b2e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBooleanArray, GetBooleanArray method [Windows Runtime], GetBooleanArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetBooleanArray method, IPropertyValue.GetBooleanArray, IPropertyValue.IPropertyValue, IPropertyValue::GetBooleanArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetBooleanArray, winrt.ipropertyvalue_getbooleanarray
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
 - IPropertyValue.GetBooleanArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of 8-bit Boolean values that is stored in the current  <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b>boolean**</b>

The array of 8-bit Boolean values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54289d10-8393-4c49-9087-873519b32aa8">CreateBooleanArray</a>



<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>
 

 

