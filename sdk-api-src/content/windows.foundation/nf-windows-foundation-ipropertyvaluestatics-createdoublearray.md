---
UID: NF:windows.foundation.IPropertyValueStatics.CreateDoubleArray
title: IPropertyValueStatics::IPropertyValueStatics (windows.foundation.h)
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified array of 64-bit floating point values.
old-location: winrt\ipropertyvaluestatics_createdoublearray.htm
tech.root: WinRT
ms.assetid: 709235a3-0699-49a2-a487-76bc5e4efb64
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateDoubleArray, CreateDoubleArray method [Windows Runtime], CreateDoubleArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateDoubleArray method, IPropertyValueStatics.CreateDoubleArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateDoubleArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateDoubleArray, winrt.ipropertyvaluefactory_createdoublearray, winrt.ipropertyvaluestatics_createdoublearray
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
 - IPropertyValueStatics.CreateDoubleArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of 64-bit floating point values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b>DOUBLE*</b>

The array of 64-bit floating point values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/197a3626-e349-4027-913c-e8203dad4fc1">IPropertyValue::GetDoubleArray</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

