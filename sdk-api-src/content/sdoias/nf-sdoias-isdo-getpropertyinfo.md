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

# ISdo::GetPropertyInfo


## -description


The 
<b>GetPropertyInfo</b> method retrieves a pointer to an <b>ISdoPropertyInfo</b> interface for the specified property.

<b>Warning:  </b>The <b>ISdoPropertyInfo</b> interface is unsupported and the use of this method to access it is discouraged.


## -parameters




### -param Id [in]

Specifies the ID of an existing property.


### -param ppPropertyInfo [out]

Pointer to a pointer that receives the address of an <b>ISdoPropertyInfo</b> interface for the specified property.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Although Server Data Objects (SDO) exposes this method, you do not need it in order to use SDO.




## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>
 

 

