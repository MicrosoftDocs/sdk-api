---
UID: NF:windows.foundation.IPropertyValueStatics.CreateDateTimeArray
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-driver-content
description: Creates a new IPropertyValue object that contains the specified array of DateTime values.
old-location: winrt\ipropertyvaluestatics_createdatetimearray.htm
old-project: WinRT
ms.assetid: 0c0beb76-0089-46b9-bcc5-ed07320859a3
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: CreateDateTimeArray, CreateDateTimeArray method [Windows Runtime], CreateDateTimeArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateDateTimeArray method, IPropertyValueStatics.CreateDateTimeArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateDateTimeArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateDateTimeArray, winrt.ipropertyvaluefactory_createdatetimearray, winrt.ipropertyvaluestatics_createdatetimearray
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
-	IPropertyValueStatics.CreateDateTimeArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a>*</b>

The array of <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/76d18ef4-676c-4130-90e3-e74776e47f33">IPropertyValue::GetDateTimeArray</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

