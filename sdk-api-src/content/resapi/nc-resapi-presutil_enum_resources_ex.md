---
UID: NC:resapi.PRESUTIL_ENUM_RESOURCES_EX
title: PRESUTIL_ENUM_RESOURCES_EX
author: windows-driver-content
description: Enumerates all of the resources in a specified cluster and initiates a user-defined operation for each resource. The PRESUTIL_ENUM_RESOURCES_EX type defines a pointer to this function.
old-location: mscs\resutilenumresourcesex.htm
old-project: MsCS
ms.assetid: e9f2e203-bbfb-4b27-b9ca-ab6b6ea1e60f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PRESUTIL_ENUM_RESOURCES_EX, PRESUTIL_ENUM_RESOURCES_EX callback function [Failover Cluster], _wolf_resutilenumresourcesex, mscs.resutilenumresourcesex, resapi/PRESUTIL_ENUM_RESOURCES_EX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_ENUM_RESOURCES_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PRESUTIL_ENUM_RESOURCES_EX callback


## -description


Enumerates all of the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in a specified 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and initiates a user-defined operation for each 
    resource. The <b>PRESUTIL_ENUM_RESOURCES_EX</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

A handle to the cluster that contains  the resources to enumerate.


### -param hSelf [in, optional]

An optional handle to a cluster resource. The callback function is not invoked for a resource that is  identified by 
       <i>hSelf</i>.


### -param lpszResTypeName [in]

An optional pointer to a name of a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> that 
       narrows the scope of resources to enumerate. If <i>lpszResTypeName</i> is specified, only 
       resources of the specified type are enumerated.


### -param pResCallBack [in]

A pointer to a user-defined function that    is called for each enumerated resource. This function must 
       conform to the definition of the 
       <a href="https://msdn.microsoft.com/663b009c-92cf-4881-bae7-fb1215140581">ResourceCallbackEx</a> callback function.  Note 
       that parameter names are not part of the definition; they have been added here for clarity.

<pre class="syntax" xml:space="preserve"><code>DWORD (*LPRESOURCE_CALLBACK_EX)( 
  HCLUSTER hCluster,
  HRESOURCE hSelf, 
  HRESOURCE hEnum, 
  PVOID pParameter 
);</code></pre>




#### hCluster

The <i>hCluster</i> parameter that is passed to 
          <i>ResUtilEnumResourcesEx</i>.



#### hSelf

The <i>hSelf</i> parameter that is passed to 
          <i>ResUtilEnumResourcesEx</i>. Note that the 
          callback function is never called when <i>hSelf</i> and <i>hEnum</i> 
          refer to the same resource.



#### hEnum

A handle to the resource that currently is being enumerated. 
          <i>ResUtilEnumResourcesEx</i> opens and closes 
          this handle automatically.



#### pParameter

A generic buffer that  enables you to pass any kind of data to the callback function.


### -param pParameter [in]

A generic buffer that  enables you to pass any kind of data to the callback function. 
       <i>ResUtilEnumResourcesEx</i> does not use this 
       parameter at all; it merely passes the pointer to the callback function. Whether  you can pass 
       <b>NULL</b> for the parameter depends on how the callback function is implemented.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function immediately halts the enumeration and returns the value that is returned by the 
       callback function.




## -remarks



<i>ResUtilEnumResourcesEx</i> is a convenient and 
     easy-to-use alternative to the 
     <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> function.


#### Examples

See the example for 
     <a href="https://msdn.microsoft.com/109fefb7-a5fc-44d2-80c0-9a08ce8d91bf">ResUtilEnumResources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a>



<a href="https://msdn.microsoft.com/109fefb7-a5fc-44d2-80c0-9a08ce8d91bf">ResUtilEnumResources</a>



<a href="https://msdn.microsoft.com/663b009c-92cf-4881-bae7-fb1215140581">ResourceCallbackEx</a>
 

 

