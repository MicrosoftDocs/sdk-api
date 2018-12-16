---
UID: NF:resapi.ResUtilResourceTypesEqual
title: ResUtilResourceTypesEqual function
author: windows-sdk-content
description: Tests whether a resource type matches the resource type name of a specified resource. The PRESUTIL_RESOURCE_TYPES_EQUAL type defines a pointer to this function.
old-location: mscs\resutilresourcetypesequal.htm
tech.root: mscs
ms.assetid: 716d2174-5fa7-4868-9f33-ab6f815e6335
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_RESOURCE_TYPES_EQUAL, PRESUTIL_RESOURCE_TYPES_EQUAL function [Failover Cluster], ResUtilResourceTypesEqual, ResUtilResourceTypesEqual function [Failover Cluster], _wolf_resutilresourcetypesequal, mscs.resutilresourcetypesequal, resapi/PRESUTIL_RESOURCE_TYPES_EQUAL, resapi/ResUtilResourceTypesEqual
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilResourceTypesEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilResourceTypesEqual function


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



The  <b>ResUtilResourceTypesEqual</b> utility function compares the resource type name pointed to by <i>lpszResourceTypeName</i> with the resource type name of the resource identified by <i>hResource</i>. To perform the comparison,  <b>ResUtilResourceTypesEqual</b> passes the  <a href="https://msdn.microsoft.com/ed679b50-306e-4623-aba3-bab64cd0e671">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a> control code to the  <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function to retrieve the resource type. If the two resource type names are the same, the resource types are equal. Note that  <b>ResUtilResourceTypesEqual</b> compares the resource type name and not the resource type  <a href="https://msdn.microsoft.com/02c61e81-486c-4543-b345-a1b2dde41982">display name</a>.




## -see-also




<a href="https://msdn.microsoft.com/ed679b50-306e-4623-aba3-bab64cd0e671">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

