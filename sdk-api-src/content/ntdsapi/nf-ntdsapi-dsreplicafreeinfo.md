---
UID: NF:ntdsapi.DsReplicaFreeInfo
title: DsReplicaFreeInfo function
author: windows-sdk-content
description: Frees the replication state data structure allocated by the DsReplicaGetInfo or DsReplicaGetInfo2 functions.
old-location: ad\dsreplicafreeinfo.htm
tech.root: ad
ms.assetid: 32ce378e-a178-4970-b3bd-3887866e97af
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DsReplicaFreeInfo, DsReplicaFreeInfo function [Active Directory], ad.dsreplicafreeinfo, ntdsapi/DsReplicaFreeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsReplicaFreeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsReplicaFreeInfo function


## -description


The <b>DsReplicaFreeInfo</b> function frees the replication state data structure allocated by the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> or <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions.


## -parameters




### -param InfoType [in]

Contains one of the <a href="https://msdn.microsoft.com/88d8a164-2192-4e73-a190-aa5b5dbb1101">DS_REPL_INFO_TYPE</a> values that specifies the type of replication data structure  contained in <i>pInfo</i>. This must be the same value passed to the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> or <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function when the structure was allocated.


### -param pInfo [in]

Pointer to the replication data structure allocated by the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> or <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/88d8a164-2192-4e73-a190-aa5b5dbb1101">DS_REPL_INFO_TYPE</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

