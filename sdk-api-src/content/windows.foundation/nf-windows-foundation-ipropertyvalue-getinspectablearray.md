---
UID: NF:windows.foundation.IPropertyValue.GetInspectableArray
title: IPropertyValue::IPropertyValue
author: windows-driver-content
description: Gets the array of pointers to IInspectable objects that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getinspectablearray.htm
old-project: WinRT
ms.assetid: 0af4f31f-e121-4cb2-8e83-c774bf25cae5
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetInspectableArray, GetInspectableArray method [Windows Runtime], GetInspectableArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetInspectableArray method, IPropertyValue.GetInspectableArray, IPropertyValue.IPropertyValue, IPropertyValue::GetInspectableArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetInspectableArray, winrt.ipropertyvalue_getinspectablearray
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windows.Foundation.h
api_name:
-	IPropertyValue.GetInspectableArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of pointers to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> objects that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize




### -param value [out]

Type: <b>IInspectable**</b>

The array of pointers to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> objects.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - length [out]

Type: <b>UINT32*</b>

The number of values in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/2bcb8530-07cb-4f54-b727-e08807c3f22b">IPropertyValueStatics::CreateInspectableArray</a>
 

 

