---
UID: NF:clusapi.ClusterNetInterfaceOpenEnum
title: ClusterNetInterfaceOpenEnum function (clusapi.h)
description: Opens an enumerator for iterating through the installed network interfaces.
helpviewer_keywords: ["ClusterNetInterfaceOpenEnum","ClusterNetInterfaceOpenEnum function [Failover Cluster]","clusapi/ClusterNetInterfaceOpenEnum","mscs.clusternetinterfaceopenenum"]
old-location: mscs\clusternetinterfaceopenenum.htm
tech.root: MsCS
ms.assetid: fd300162-2472-4bd2-91d6-357397c4134c
ms.date: 12/05/2018
ms.keywords: ClusterNetInterfaceOpenEnum, ClusterNetInterfaceOpenEnum function [Failover Cluster], clusapi/ClusterNetInterfaceOpenEnum, mscs.clusternetinterfaceopenenum
f1_keywords:
- clusapi/ClusterNetInterfaceOpenEnum
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClusAPI.dll
api_name:
- ClusterNetInterfaceOpenEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterNetInterfaceOpenEnum function


## -description


Opens an 
    enumerator for iterating through the installed <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-interfaces">network interfaces</a>.


## -parameters




### -param hCluster [in]

Handle to a cluster


### -param lpszNodeName [in, optional]

The name of the node.


### -param lpszNetworkName [in, optional]

The name of the network.


## -returns



If the operation succeeds, returns a handle to an 
       enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.



