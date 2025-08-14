---
UID: NF:clusapi.ClusterNetInterfaceCloseEnum
title: ClusterNetInterfaceCloseEnum function (clusapi.h)
description: Closes a network interface enumeration handle.
helpviewer_keywords: ["ClusterNetInterfaceCloseEnum","ClusterNetInterfaceCloseEnum function [Failover Cluster]","clusapi/ClusterNetInterfaceCloseEnum","mscs.clusternetinterfacecloseenum"]
old-location: mscs\clusternetinterfacecloseenum.htm
tech.root: MsCS
ms.assetid: da7819b5-0f18-44e3-83e7-f6d5ccbc0de6
ms.date: 12/05/2018
ms.keywords: ClusterNetInterfaceCloseEnum, ClusterNetInterfaceCloseEnum function [Failover Cluster], clusapi/ClusterNetInterfaceCloseEnum, mscs.clusternetinterfacecloseenum
req.header: clusapi.h
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterNetInterfaceCloseEnum
 - clusapi/ClusterNetInterfaceCloseEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ClusAPI.dll
api_name:
 - ClusterNetInterfaceCloseEnum
---

# ClusterNetInterfaceCloseEnum function


## -description

Closes a  network interface enumeration handle.

## -parameters

### -param hNetInterfaceEnum [in]

Handle to the node enumerator to close. This is a handle originally returned by the  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusternetinterfaceopenenum">ClusterNetInterfaceOpenEnum</a> function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.