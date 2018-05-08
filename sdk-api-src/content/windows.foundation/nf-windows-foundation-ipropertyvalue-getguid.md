---
UID: NF:windows.foundation.IPropertyValue.GetGuid
title: IPropertyValue::IPropertyValue
author: windows-driver-content
description: Gets the GUID value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getguid.htm
old-project: WinRT
ms.assetid: d094f70f-dfd3-4601-b288-4f9f79479609
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetGuid, GetGuid method [Windows Runtime], GetGuid method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetGuid method, IPropertyValue.GetGuid, IPropertyValue.IPropertyValue, IPropertyValue::GetGuid, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetGuid, winrt.ipropertyvalue_getguid
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
-	IPropertyValue.GetGuid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValue::IPropertyValue


## -description


Gets the GUID value that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param value [out, retval]

Type: <b>GUID*</b>

The value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/fb895839-953f-41e2-963a-26156c490df0">IPropertyValueStatics::CreateGuid</a>
 

 

