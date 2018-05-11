---
UID: NF:clusapi.ClusterRegCloseKey
title: ClusterRegCloseKey function
author: windows-driver-content
description: Releases the handle of a cluster database key.
old-location: mscs\clusterregclosekey.htm
old-project: MsCS
ms.assetid: 2216ac42-6beb-4ceb-bd15-12bb2886bc6a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ClusterRegCloseKey, ClusterRegCloseKey function [Failover Cluster], _wolf_clusterregclosekey, clusapi/ClusterRegCloseKey, mscs.clusterregclosekey
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
-	ClusterRegCloseKey
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegCloseKey function


## -description


Releases the handle of a  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to the cluster database key to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>
 

 

