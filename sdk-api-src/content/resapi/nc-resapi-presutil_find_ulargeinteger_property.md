---
UID: NC:resapi.PRESUTIL_FIND_ULARGEINTEGER_PROPERTY
title: PRESUTIL_FIND_ULARGEINTEGER_PROPERTY
author: windows-sdk-content
description: Gets a large integer property value from a property list. The PRESUTIL_FIND_ULARGEINTEGER_PROPERTY type defines a pointer to this function.
old-location: mscs\resutilfindulargeintegerproperty.htm
old-project: MsCS
ms.assetid: BA4DD6F0-07DB-4601-B8EB-E79B49F2829F
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_FIND_ULARGEINTEGER_PROPERTY, PRESUTIL_FIND_ULARGEINTEGER_PROPERTY callback, PRESUTIL_FIND_ULARGEINTEGER_PROPERTY callback function [Failover Cluster], mscs.resutilfindulargeintegerproperty, resapi/PRESUTIL_FIND_ULARGEINTEGER_PROPERTY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_FIND_ULARGEINTEGER_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

