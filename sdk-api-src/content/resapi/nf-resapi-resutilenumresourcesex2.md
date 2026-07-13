---
UID: NF:resapi.ResUtilEnumResourcesEx2
title: ResUtilEnumResourcesEx2 function (resapi.h)
description: Enumerates all of the resources in a specified cluster and initiates a user-defined operation for each resource. The PRESUTIL_ENUM_RESOURCES_EX2 type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_ENUM_RESOURCES_EX2","PRESUTIL_ENUM_RESOURCES_EX2 function [Failover Cluster]","ResUtilEnumResourcesEx2","ResUtilEnumResourcesEx2 function [Failover Cluster]","mscs.resutilenumresourcesex2","resapi/PRESUTIL_ENUM_RESOURCES_EX2","resapi/ResUtilEnumResourcesEx2"]
old-location: mscs\resutilenumresourcesex2.htm
tech.root: MsCS
ms.assetid: F178850C-D68A-4A51-A830-F12E023352B4
ms.date: 12/05/2018
ms.keywords: PRESUTIL_ENUM_RESOURCES_EX2, PRESUTIL_ENUM_RESOURCES_EX2 function [Failover Cluster], ResUtilEnumResourcesEx2, ResUtilEnumResourcesEx2 function [Failover Cluster], mscs.resutilenumresourcesex2, resapi/PRESUTIL_ENUM_RESOURCES_EX2, resapi/ResUtilEnumResourcesEx2
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - ResUtilEnumResourcesEx2
 - resapi/ResUtilEnumResourcesEx2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilEnumResourcesEx2
---

# ResUtilEnumResourcesEx2 function


## -description

Enumerates all of the <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> in a specified 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and initiates a user-defined operation for each 
    resource. The <b>PRESUTIL_ENUM_RESOURCES_EX2</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

A handle to the cluster that contains the resources to enumerate.

### -param hSelf [in, optional]

An optional handle to a cluster resource. The callback function is not invoked for a resource identified by 
       <i>hSelf</i>.

### -param lpszResTypeName [in]

An optional pointer to a name of a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> that 
       narrows the scope of resources to enumerate. If <i>lpszResTypeName</i> is specified, only 
       resources of the specified type are enumerated.

### -param pResCallBack [in]

A pointer to a user-defined function which will be called for each enumerated resource. This function must 
       conform to the definition of the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-lpresource_callback_ex">ResourceCallbackEx</a> callback function (note 
       that parameter names are not part of the definition; they have been added here for clarity):


``` syntax
DWORD (*LPRESOURCE_CALLBACK_EX)( 
  HCLUSTER hCluster,
  HRESOURCE hSelf, 
  HRESOURCE hEnum, 
  PVOID pParameter 
);
```





#### hCluster

[in] The hCluster parameter passed to 
          <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresourcesex">ResUtilEnumResourcesEx</a>.



#### hSelf

[in] The hSelf parameter passed to 
          <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresourcesex">ResUtilEnumResourcesEx</a>. Note that the 
          callback function is never called when <i>hSelf</i> and <i>hEnum</i> 
          refer to the same resource.



#### hEnum

[in] A handle to the resource currently being enumerated. 
          <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresourcesex">ResUtilEnumResourcesEx</a> opens and closes 
          this handle automatically.



#### pParameter

[in] A generic buffer that allows you to pass any kind of data to the callback function.

### -param pParameter [in]

A generic buffer that allows you to pass any kind of data to the callback function. 
       <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresourcesex">ResUtilEnumResourcesEx</a> does not use this 
       parameter at all, it merely passes the pointer to the callback function. Whether or not you can pass 
       <b>NULL</b> for the parameter depends on how the callback function is implemented.

### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error may be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresourcesex">ResUtilEnumResourcesEx</a>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function immediately halts the enumeration and returns the value returned by the 
       callback function.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>
