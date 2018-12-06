---
UID: NF:windows.foundation.IPropertyValue.GetChar16Array
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the the array of Unicode characters that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getchar16array.htm
tech.root: WinRT
ms.assetid: b0649a8b-8060-4e0f-956e-879fe4185b11
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetChar16Array, GetChar16Array method [Windows Runtime], GetChar16Array method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetChar16Array method, IPropertyValue.GetChar16Array, IPropertyValue.IPropertyValue, IPropertyValue::GetChar16Array, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetChar16Array, winrt.ipropertyvalue_getchar16array
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
 - IPropertyValue.GetChar16Array
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the the array of Unicode characters that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of Unicode characters in the array.


### -param value [out]

Type: <b>WCHAR**</b>

The array of Unicode characters.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/4d78015a-dfe1-49be-8523-a5b0f96f7c58">IPropertyValueStatics::CreateChar16Array</a>
 

 

