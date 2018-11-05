---
UID: NF:windows.foundation.IPropertyValueStatics.CreateRect
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified Rect value.
old-location: winrt\ipropertyvaluestatics_createrect.htm
tech.root: WinRT
ms.assetid: 2938c3e0-6383-4136-99a6-c47a04c331f7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateRect, CreateRect method [Windows Runtime], CreateRect method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateRect method, IPropertyValueStatics.CreateRect, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateRect, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateRect, winrt.ipropertyvaluefactory_createrect, winrt.ipropertyvaluestatics_createrect
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
 - IPropertyValueStatics.CreateRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> value.


## -parameters




### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a></b>

The value to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2333bd80-56db-4fa4-b696-269969fd1362">IPropertyValue::GetRect</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

