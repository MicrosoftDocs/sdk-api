---
UID: NF:windows.foundation.IPropertyValue.GetUInt8Array
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of unsigned 8-bit integer values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getuint8array.htm
tech.root: WinRT
ms.assetid: f17fe310-40b7-46a5-ae87-c07649c2f288
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetUInt8Array, GetUInt8Array method [Windows Runtime], GetUInt8Array method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetUInt8Array method, IPropertyValue.GetUInt8Array, IPropertyValue.IPropertyValue, IPropertyValue::GetUInt8Array, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetUInt8Array, winrt.ipropertyvalue_getuint8array
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
 - IPropertyValue.GetUInt8Array
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of unsigned 8-bit integer values that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize

TBD


### -param value [out]

Type: <b>BYTE**</b>

The array of unsigned 8-bit integer values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - length [out]

Type: <b>UINT32*</b>

The number of values in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/fc666379-4992-47da-b97b-b296219e26c1">IPropertyValueStatics::CreateUInt8Array</a>
 

 

