---
UID: NC:clusapi.PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX
title: PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX
author: windows-sdk-content
description: Closes a node enumeration handle.
old-location: mscs\clusternodecloseenumex.htm
old-project: mscs
ms.assetid: 1B743E4E-F8E0-4E73-B5FA-53D4FC547251
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterNodeCloseEnumEx, ClusterNodeCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterNodeCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX, mscs.clusternodecloseenumex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterNodeCloseEnumEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX callback function


## -description


Closes a 
node enumeration handle.


## -parameters




### -param hNodeEnum [in]

The handle to the node enumeration  to close. This handle is returned by the  <a href="https://msdn.microsoft.com/A251C5A3-2C9F-4030-8013-4846AD83A2E9">ClusterNodeOpenEnumEx</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>
 

 

