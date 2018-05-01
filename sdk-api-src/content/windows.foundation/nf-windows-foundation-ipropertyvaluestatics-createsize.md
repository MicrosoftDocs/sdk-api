---
UID: NF:windows.foundation.IPropertyValueStatics.CreateSize
title: IPropertyValueStatics::CreateSize method
author: windows-driver-content
description: Creates a new IPropertyValue object that contains the specified Size value.
old-location: winrt\ipropertyvaluestatics_createsize.htm
old-project: WinRT
ms.assetid: 0a5055f1-6873-4396-9a3e-b7a4cc41200e
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CreateSize method [Windows Runtime], CreateSize method [Windows Runtime], IPropertyValueStatics interface, CreateSize,IPropertyValueStatics.CreateSize, IPropertyValueStatics, IPropertyValueStatics interface [Windows Runtime], CreateSize method, IPropertyValueStatics::CreateSize, windows/IPropertyValueStatics::CreateSize, winrt.ipropertyvaluefactory_createsize, winrt.ipropertyvaluestatics_createsize
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
-	IPropertyValueStatics.CreateSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValueStatics::CreateSize method


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a> value.


## -parameters




### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a></b>

The value to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c864cf0e-8e7e-44b0-93dc-3d2d9f2326a7">IPropertyValue::GetSize</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

