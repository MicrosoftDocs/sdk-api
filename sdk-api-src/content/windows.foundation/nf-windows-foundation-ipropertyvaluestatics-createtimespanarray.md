---
UID: NF:windows.foundation.IPropertyValueStatics.CreateTimeSpanArray
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified array of TimeSpan values.
old-location: winrt\ipropertyvaluestatics_createtimespanarray.htm
tech.root: WinRT
ms.assetid: 3f663acc-5ced-4fd2-a0d5-3e462fe60251
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateTimeSpanArray, CreateTimeSpanArray method [Windows Runtime], CreateTimeSpanArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateTimeSpanArray method, IPropertyValueStatics.CreateTimeSpanArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateTimeSpanArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateTimeSpanArray, winrt.ipropertyvaluefactory_createtimespanarray, winrt.ipropertyvaluestatics_createtimespanarray
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
 - IPropertyValueStatics.CreateTimeSpanArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a>*</b>

The array of <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a52a665c-4c3a-4489-bd7b-e8ecb8dfe9cc">IPropertyValue::GetTimeSpanArray</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

