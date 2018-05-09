---
UID: NF:clusapi.ClusterRegReadBatchAddCommand
title: ClusterRegReadBatchAddCommand function
author: windows-driver-content
description: Adds a read command to a batch that executes on a cluster registry key.
old-location: mscs\clusterregreadbatchaddcommand.htm
old-project: MsCS
ms.assetid: 2B665231-7325-43C4-92A4-4EDF28126BA1
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ClusterRegReadBatchAddCommand, ClusterRegReadBatchAddCommand function [Failover Cluster], clusapi/ClusterRegReadBatchAddCommand, mscs.clusterregreadbatchaddcommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
-	ClusterRegReadBatchAddCommand
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegReadBatchAddCommand function


## -description


Adds a read command to a batch that executes on a cluster registry key.


## -parameters




### -param hRegReadBatch [in]

The handle of the read batch to which a command will be added. Create a batch by calling the <a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a> function.


### -param wzSubkeyName [in, optional]

The name of the key relative to the cluster registry key. If this name is <b>NULL</b>, the read is performed on the cluster registry key represented in the <i>hRegReadBatch</i> parameter.


### -param wzValueName [in, optional]

The name of the registry value to be read. If this name is <b>NULL</b>, the content of the default value is returned.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



Additional calls to the <b>ClusterRegReadBatchAddCommand</b> function add additional read commands to the batch.




## -see-also




<a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a>
 

 

