---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemPropertyProvider::PutProperty


## -description


The <b>IWbemPropertyProvider::PutProperty</b> method is called by Windows Management to update a property value supported by a property provider.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param strLocale [in]

String indicating the desired locale in cases where the returned property value can be localized. If the property cannot be localized, the implementation can ignore this value.


### -param strClassMapping [in]

Literal copy of the string value for the <b>ClassContext</b> qualifier for the class. This points to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.


### -param strInstMapping [in]

Literal copy of the string value for the <b>InstanceContext</b> qualifier for the instance. This must point to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.


### -param strPropMapping [in]

Literal copy of the value of the <b>PropertyContext</b> qualifier for the property. This must point to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.


### -param pvValue [in]

Pointer to an existing <b>VARIANT</b> that contains the value to be written.


## -returns



This method must return <b>WBEM_S_NO_ERROR</b> if the operation succeeds, or <b>WBEM_S_FALSE</b> if the operation fails.




## -see-also




<a href="https://msdn.microsoft.com/6ee0e904-7f4c-4b32-8a90-d727340b481e">GetProperty</a>
 

 

