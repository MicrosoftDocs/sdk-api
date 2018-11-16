---
UID: NF:windows.foundation.IPropertyValueStatics.CreateBooleanArray
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified array of 8-bit Boolean values.
old-location: winrt\ipropertyvaluestatics_createbooleanarray.htm
tech.root: WinRT
ms.assetid: 54289d10-8393-4c49-9087-873519b32aa8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateBooleanArray, CreateBooleanArray method [Windows Runtime], CreateBooleanArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateBooleanArray method, IPropertyValueStatics.CreateBooleanArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateBooleanArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateBooleanArray, winrt.ipropertyvaluefactory_createbooleanarray, winrt.ipropertyvaluestatics_createbooleanarray
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
 - IPropertyValueStatics.CreateBooleanArray
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
- IPropertyValueStatics.CreateBooleanArray
: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of 8-bit Boolean values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b>boolean*</b>

The array of 8-bit Boolean values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/22ad7bab-87b1-41e8-ae65-1957e7c93b2e">IPropertyValue::GetBooleanArray</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

