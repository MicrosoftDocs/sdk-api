---
UID: NF:windows.foundation.IPropertyValue.GetDateTimeArray
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of DateTime values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getdatetimearray.htm
tech.root: WinRT
ms.assetid: 76d18ef4-676c-4130-90e3-e74776e47f33
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetDateTimeArray, GetDateTimeArray method [Windows Runtime], GetDateTimeArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetDateTimeArray method, IPropertyValue.GetDateTimeArray, IPropertyValue.IPropertyValue, IPropertyValue::GetDateTimeArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetDateTimeArray, winrt.ipropertyvalue_getdatetimearray
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
 - IPropertyValue.GetDateTimeArray
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
- IPropertyValue.GetDateTimeArray
: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> values that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a>**</b>

The array of <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/0c0beb76-0089-46b9-bcc5-ed07320859a3">IPropertyValueStatics::CreateDateTimeArray</a>
 

 

