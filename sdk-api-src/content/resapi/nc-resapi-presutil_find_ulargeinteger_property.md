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

# PRESUTIL_FIND_ULARGEINTEGER_PROPERTY callback function


## -description


Gets a large integer property value from a property list. The <b>PRESUTIL_FIND_ULARGEINTEGER_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param pPropertyList [in]

A pointer to the property list.


### -param cbPropertyListSize [in]

The size of the data in <i>pPropertyList</i>, in bytes.


### -param pszPropertyName [in]

The name of the property.


### -param *plPropertyValue [out]

The value of the property.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error 
       code.




## -see-also




<a href="https://msdn.microsoft.com/b6287135-e9b3-43ab-aaf4-1488dad3e9ed">Property List Parsing Functions</a>
 

 

