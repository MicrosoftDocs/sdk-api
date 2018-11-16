---
UID: NF:clusapi.GetClusterResourceKey
title: GetClusterResourceKey function
author: windows-sdk-content
description: Opens the root of the cluster database subtree for a resource.
old-location: mscs\getclusterresourcekey.htm
tech.root: MsCS
ms.assetid: 841f28a1-1415-41bb-b8ac-cf17c6d7c6f3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetClusterResourceKey, GetClusterResourceKey function [Failover Cluster], _wolf_getclusterresourcekey, clusapi/GetClusterResourceKey, mscs.getclusterresourcekey
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
 - GetClusterResourceKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetClusterResourceKey
: 
---

# GetClusterResourceKey function


## -description


Opens the root of the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> subtree for a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -parameters




### -param hResource [in]

Handle to a resource.


### -param samDesired [in]

Access mask that describes the security access needed for the opened key.


## -returns



If the operation succeeds, the function returns a registry key handle for the resource.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <b>GetClusterResourceKey</b> function returns a handle to a cluster database key representing the subtree root for the resource identified by <i>hResource</i>. Callers should call  <a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterResourceKey</b> when they are done with it.




## -see-also




<a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

