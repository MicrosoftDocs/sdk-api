---
UID: NF:windows.foundation.IPropertyValueStatics.CreateGuid
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-driver-content
description: Creates a new IPropertyValue object that contains the specified GUID value.
old-location: winrt\ipropertyvaluestatics_createguid.htm
old-project: WinRT
ms.assetid: fb895839-953f-41e2-963a-26156c490df0
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: CreateGuid, CreateGuid method [Windows Runtime], CreateGuid method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateGuid method, IPropertyValueStatics.CreateGuid, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateGuid, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateGuid, winrt.ipropertyvaluefactory_createguid, winrt.ipropertyvaluestatics_createguid
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
-	IPropertyValueStatics.CreateGuid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <b>GUID</b> value.


## -parameters




### -param value [in]

Type: <b>GUID</b>

The value to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d094f70f-dfd3-4601-b288-4f9f79479609">IPropertyValue::GetGuid</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

