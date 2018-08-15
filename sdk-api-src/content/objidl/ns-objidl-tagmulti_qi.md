---
UID: NS:objidl.tagMULTI_QI
title: tagMULTI_QI
author: windows-sdk-content
description: Represents an interface in a query for multiple interfaces.
old-location: com\multi_qi.htm
old-project: com
ms.assetid: 845040c9-fad4-4ac8-856d-d35edbf48ec9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MULTI_QI, MULTI_QI structure [COM], _com_MULTI_QI, com.multi_qi, objidlbase/MULTI_QI, tagMULTI_QI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: Objidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MULTI_QI
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - MULTI_QI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagMULTI_QI structure


## -description


Represents an interface in a query for multiple interfaces.


## -struct-fields




### -field pIID

A pointer to an interface identifier.


### -field pItf

A pointer to the interface requested in <b>pIID</b>. This member must be <b>NULL</b> on input.


### -field hr

The return value of the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call to locate the requested interface. Common return values include S_OK and E_NOINTERFACE. This member must be 0 on input.


## -remarks



To optimize network performance, most remote activation functions take an array of <b>MULTI_QI</b> structures rather than just a single IID as input and a single pointer to the requested interface on the object as output, as do local activation functions. This allows a set of pointers to interfaces to be returned from the same object in a single round-trip to the server. In network scenarios, requesting multiple interfaces at the time of object construction can save considerable time over using a number of calls to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for unique interfaces, each of which would require a round-trip to the server.

 




## -see-also




<a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>



<a href="https://msdn.microsoft.com/f8a22f5f-a21f-49e7-bd6c-ca987206ee46">CoGetInstanceFromFile</a>



<a href="https://msdn.microsoft.com/6a77770c-b7e1-4d29-9c4b-331b5950a635">CoGetInstanceFromIStorage</a>



<a href="https://msdn.microsoft.com/5e50396f-2931-403f-946a-dc096cb012cc">IMultiQI</a>
 

 

