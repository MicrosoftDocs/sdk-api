---
UID: NF:windows.foundation.IPropertyValueStatics.CreatePointArray
title: IPropertyValueStatics::CreatePointArray method
author: windows-driver-content
description: Creates a new IPropertyValue object that contains the specified array of Point values.
old-location: winrt\ipropertyvaluestatics_createpointarray.htm
old-project: WinRT
ms.assetid: cdfc2a91-0f1b-41d9-99e3-e3589bdae6ca
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CreatePointArray method [Windows Runtime], CreatePointArray method [Windows Runtime], IPropertyValueStatics interface, CreatePointArray,IPropertyValueStatics.CreatePointArray, IPropertyValueStatics, IPropertyValueStatics interface [Windows Runtime], CreatePointArray method, IPropertyValueStatics::CreatePointArray, windows/IPropertyValueStatics::CreatePointArray, winrt.ipropertyvaluefactory_createpointarray, winrt.ipropertyvaluestatics_createpointarray
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
-	IPropertyValueStatics.CreatePointArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValueStatics::CreatePointArray method


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a> values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>*</b>

The array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a> values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7df4ad4e-3ca6-4956-b907-02c2cb6e481b">IPropertyValue::GetPointArray</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

