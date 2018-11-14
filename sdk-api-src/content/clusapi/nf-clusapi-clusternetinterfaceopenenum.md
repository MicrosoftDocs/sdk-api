---
UID: NF:clusapi.ClusterNetInterfaceOpenEnum
title: ClusterNetInterfaceOpenEnum function
author: windows-sdk-content
description: Opens an enumerator for iterating through the installed network interfaces.
old-location: mscs\clusternetinterfaceopenenum.htm
tech.root: mscs
ms.assetid: fd300162-2472-4bd2-91d6-357397c4134c
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ClusterNetInterfaceOpenEnum, ClusterNetInterfaceOpenEnum function [Failover Cluster], clusapi/ClusterNetInterfaceOpenEnum, mscs.clusternetinterfaceopenenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterNetInterfaceOpenEnum
: 
---

# ClusterNetInterfaceOpenEnum function


## -description


Opens an 
    enumerator for iterating through the installed <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a>.


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
       error, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.



