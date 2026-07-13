---
UID: NF:resapi.ResUtilGetResourceName
title: ResUtilGetResourceName function (resapi.h)
description: Returns the name of a resource. The PRESUTIL_GET_RESOURCE_NAME type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_NAME","PRESUTIL_GET_RESOURCE_NAME function [Failover Cluster]","ResUtilGetResourceName","ResUtilGetResourceName function [Failover Cluster]","_wolf_resutilgetresourcename","mscs.resutilgetresourcename","resapi/PRESUTIL_GET_RESOURCE_NAME","resapi/ResUtilGetResourceName"]
old-location: mscs\resutilgetresourcename.htm
tech.root: MsCS
ms.assetid: 968d013f-6502-4981-982e-7b3f10c53b60
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_NAME, PRESUTIL_GET_RESOURCE_NAME function [Failover Cluster], ResUtilGetResourceName, ResUtilGetResourceName function [Failover Cluster], _wolf_resutilgetresourcename, mscs.resutilgetresourcename, resapi/PRESUTIL_GET_RESOURCE_NAME, resapi/ResUtilGetResourceName
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
 - ResUtilGetResourceName
 - resapi/ResUtilGetResourceName
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
 - ResUtilGetResourceName
---

# ResUtilGetResourceName function


## -description

Returns the name of a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The 
    <b>PRESUTIL_GET_RESOURCE_NAME</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Resource handle (see 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>).

### -param pszResourceName [out]

Pointer to a buffer that receives the resource name.

### -param pcchResourceNameInOut [in, out]

On input, specifies the size of the buffer pointed to by <i>pszResourceName</i>, in wide 
      characters. On output, specifies the actual size of the resource name returned as a count of wide 
      characters.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.