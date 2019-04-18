---
UID: NF:windows.foundation.IPropertyValueStatics.CreateStringArray
title: IPropertyValueStatics::IPropertyValueStatics (windows.foundation.h)
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified array of string values.
old-location: winrt\ipropertyvaluestatics_createstringarray.htm
tech.root: WinRT
ms.assetid: b9741a88-4585-4eda-b21d-5af0e541ef48
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateStringArray, CreateStringArray method [Windows Runtime], CreateStringArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateStringArray method, IPropertyValueStatics.CreateStringArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateStringArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateStringArray, winrt.ipropertyvaluefactory_createstringarray, winrt.ipropertyvaluestatics_createstringarray
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
 - IPropertyValueStatics.CreateStringArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of string values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

The array of string values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d256b888-efa0-470e-b54f-5cf8ddd6fd8a">IPropertyValue::GetStringArray</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

