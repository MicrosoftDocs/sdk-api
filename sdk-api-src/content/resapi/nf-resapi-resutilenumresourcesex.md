---
UID: NF:resapi.ResUtilEnumResourcesEx
title: ResUtilEnumResourcesEx function (resapi.h)
description: Enumerates all of the resources in a specified cluster and initiates a user-defined operation for each resource. The PRESUTIL_ENUM_RESOURCES_EX type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_ENUM_RESOURCES_EX","PRESUTIL_ENUM_RESOURCES_EX function [Failover Cluster]","ResUtilEnumResourcesEx","ResUtilEnumResourcesEx function [Failover Cluster]","_wolf_resutilenumresourcesex","mscs.resutilenumresourcesex","resapi/PRESUTIL_ENUM_RESOURCES_EX","resapi/ResUtilEnumResourcesEx"]
old-location: mscs\resutilenumresourcesex.htm
tech.root: MsCS
ms.assetid: e9f2e203-bbfb-4b27-b9ca-ab6b6ea1e60f
ms.date: 12/05/2018
ms.keywords: PRESUTIL_ENUM_RESOURCES_EX, PRESUTIL_ENUM_RESOURCES_EX function [Failover Cluster], ResUtilEnumResourcesEx, ResUtilEnumResourcesEx function [Failover Cluster], _wolf_resutilenumresourcesex, mscs.resutilenumresourcesex, resapi/PRESUTIL_ENUM_RESOURCES_EX, resapi/ResUtilEnumResourcesEx
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilEnumResourcesEx
 - resapi/ResUtilEnumResourcesEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ext-ms-win-cluster-resutils-l1-1-2.dll
 - ResUtils.dll
 - Ext-MS-Win-Cluster-Resutils-L1-1-1.dll
api_name:
 - ResUtilEnumResourcesEx
---

# ResUtilEnumResourcesEx function


## -description

Enumerates all of the <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> in a specified 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and initiates a user-defined operation for each 
    resource. The <b>PRESUTIL_ENUM_RESOURCES_EX</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

A handle to the cluster that contains  the resources to enumerate.

### -param hSelf [in, optional]

An optional handle to a cluster resource. The callback function is not invoked for a resource that is  identified by 
       <i>hSelf</i>.

### -param lpszResTypeName [in]

An optional pointer to a name of a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> that 
       narrows the scope of resources to enumerate. If <i>lpszResTypeName</i> is specified, only 
       resources of the specified type are enumerated.

### -param pResCallBack [in]

A pointer to a user-defined function that    is called for each enumerated resource. This function must 
       conform to the definition of the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-lpresource_callback_ex">ResourceCallbackEx</a> callback function.  Note 
       that parameter names are not part of the definition; they have been added here for clarity.


``` syntax
DWORD (*LPRESOURCE_CALLBACK_EX)( 
  HCLUSTER hCluster,
  HRESOURCE hSelf, 
  HRESOURCE hEnum, 
  PVOID pParameter 
);
```





#### hCluster

The <i>hCluster</i> parameter that is passed to 
          <b>ResUtilEnumResourcesEx</b>.



#### hSelf

The <i>hSelf</i> parameter that is passed to 
          <b>ResUtilEnumResourcesEx</b>. Note that the 
          callback function is never called when <i>hSelf</i> and <i>hEnum</i> 
          refer to the same resource.



#### hEnum

A handle to the resource that currently is being enumerated. 
          <b>ResUtilEnumResourcesEx</b> opens and closes 
          this handle automatically.



#### pParameter

A generic buffer that  enables you to pass any kind of data to the callback function.

### -param pParameter [in]

A generic buffer that  enables you to pass any kind of data to the callback function. 
       <b>ResUtilEnumResourcesEx</b> does not use this 
       parameter at all; it merely passes the pointer to the callback function. Whether  you can pass 
       <b>NULL</b> for the parameter depends on how the callback function is implemented.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function immediately halts the enumeration and returns the value that is returned by the 
       callback function.

## -remarks

<b>ResUtilEnumResourcesEx</b> is a convenient and 
     easy-to-use alternative to the 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> function.


#### Examples

See the example for 
     <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresources">ResUtilEnumResources</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresources">ResUtilEnumResources</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-lpresource_callback_ex">ResourceCallbackEx</a>
