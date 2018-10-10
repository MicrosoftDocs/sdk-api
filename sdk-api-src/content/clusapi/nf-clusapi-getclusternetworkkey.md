---
UID: NF:clusapi.GetClusterNetworkKey
title: GetClusterNetworkKey function
author: windows-sdk-content
description: Opens the root of the cluster database subtree for a network.
old-location: mscs\getclusternetworkkey.htm
tech.root: MsCS
ms.assetid: c5d914b4-0419-4c03-bed4-ecb87e44db5e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetClusterNetworkKey, GetClusterNetworkKey function [Failover Cluster], _wolf_getclusternetworkkey, clusapi/GetClusterNetworkKey, mscs.getclusternetworkkey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
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
 - GetClusterNetworkKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNetworkKey function


## -description


Opens the root of the  <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> subtree for a  <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>.


## -parameters




### -param hNetwork [in]

Handle to a network.


### -param samDesired [in]

Access mask that describes the security access needed for the new key.


## -returns



If the operation succeeds, the function returns a registry key handle for the network.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <b>GetClusterNetworkKey</b> function returns a handle to a cluster database key representing the subtree root for the network identified by <i>hNetwork</i>. Callers should call  <a href="https://msdn.microsoft.com/en-us/library/Aa368989(v=VS.85).aspx">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterNetworkKey</b> when they are done with it.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368989(v=VS.85).aspx">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

