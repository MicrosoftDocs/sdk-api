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

# ISdo::PutProperty


## -description


The 
<b>PutProperty</b> method sets the value of the specified property.


## -parameters




### -param Id [in]

Specifies the ID of an existing property.


### -param pValue [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> that contains the value for that property.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



After you have set values using <b>ISdo::PutProperty</b>, call 
<a href="https://msdn.microsoft.com/aceca2f9-7b17-46a5-bcd1-e6fec3c369ed">ISdo::Apply</a> to write the changes to persistent storage.

The method fails if the property is READ_ONLY or if the value is invalid.




## -see-also




<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/aceca2f9-7b17-46a5-bcd1-e6fec3c369ed">ISdo::Apply</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

