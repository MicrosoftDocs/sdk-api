---
UID: NF:windows.foundation.IPropertyValueStatics.CreateTimeSpan
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified TimeSpan value.
old-location: winrt\ipropertyvaluestatics_createtimespan.htm
tech.root: WinRT
ms.assetid: eae11d63-c909-45fc-a38f-d9599b873b6f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateTimeSpan, CreateTimeSpan method [Windows Runtime], CreateTimeSpan method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateTimeSpan method, IPropertyValueStatics.CreateTimeSpan, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateTimeSpan, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateTimeSpan, winrt.ipropertyvaluefactory_createtimespan, winrt.ipropertyvaluestatics_createtimespan
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
 - IPropertyValueStatics.CreateTimeSpan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> value.


## -parameters




### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a></b>

The value to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c78d584f-e2ef-4623-b45a-e26d2ec1518b">IPropertyValue::GetTimeSpan</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

