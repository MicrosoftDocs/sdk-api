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

# PRESUTIL_RESOURCE_TYPES_EQUAL callback function


## -description


Tests whether a  <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> matches the resource type name of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The <b>PRESUTIL_RESOURCE_TYPES_EQUAL</b> type defines a pointer to this function.


## -parameters




### -param lpszResourceTypeName [in]

Pointer to the resource type name to test.


### -param hResource [in]

Handle of the resource to test.


## -returns



If the resource types are equal, the function returns <b>TRUE</b>.

If the resource types are not equal, 
the function returns <b>FALSE</b>.




## -remarks



The  <i>ResUtilResourceTypesEqual</i> utility function compares the resource type name pointed to by <i>lpszResourceTypeName</i> with the resource type name of the resource identified by <i>hResource</i>. To perform the comparison,  <i>ResUtilResourceTypesEqual</i> passes the  <a href="https://msdn.microsoft.com/ed679b50-306e-4623-aba3-bab64cd0e671">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a> control code to the  <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function to retrieve the resource type. If the two resource type names are the same, the resource types are equal. Note that  <i>ResUtilResourceTypesEqual</i> compares the resource type name and not the resource type  <a href="https://msdn.microsoft.com/02c61e81-486c-4543-b345-a1b2dde41982">display name</a>.




## -see-also




<a href="https://msdn.microsoft.com/ed679b50-306e-4623-aba3-bab64cd0e671">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

