---
UID: NF:clusapi.GetClusterResourceTypeKey
title: GetClusterResourceTypeKey function
author: windows-sdk-content
description: Opens the root of the cluster database subtree for a resource type.
old-location: mscs\getclusterresourcetypekey.htm
old-project: MsCS
ms.assetid: facc22b2-221d-4d82-85ae-5b9a463c5858
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetClusterResourceTypeKey, GetClusterResourceTypeKey function [Failover Cluster], _wolf_getclusterresourcetypekey, clusapi/GetClusterResourceTypeKey, mscs.getclusterresourcetypekey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - GetClusterResourceTypeKey
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# GetClusterResourceTypeKey function


## -description


Opens the root of the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> subtree for a  <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


### -param lpszTypeName [in]

Pointer to a NULL-terminated Unicode string specifying the name of a resource type (the registered type name, not the display name).


### -param samDesired [in]

Access mask that describes the security access needed for the opened key.


## -returns



If the operation succeeds, the function returns a registry key handle for the resource type.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <b>GetClusterResourceTypeKey</b> function returns a handle to a cluster database key representing the subtree root for the resource type pointed to by <i>lpszTypeName</i> in the cluster identified by <i>hCluster</i>. Callers should call  <a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterResourceTypeKey</b> when they are done with it.




## -see-also




<a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

