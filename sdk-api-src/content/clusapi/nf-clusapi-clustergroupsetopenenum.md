---
UID: NF:clusapi.ClusterGroupSetOpenEnum
title: ClusterGroupSetOpenEnum function (clusapi.h)
author: windows-sdk-content
description: Starts the enumeration of groupset for a cluster.
old-location: mscs\clustergroupcollectionopenenum.htm
tech.root: MsCS
ms.assetid: 9e629cc8-2e5f-4682-a9b5-902d13a9792d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterGroupSetOpenEnum, ClusterGroupSetOpenEnum function [Failover Cluster], clusapi/ClusterGroupSetOpenEnum, mscs.clustergroupcollectionopenenum
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
 - ClusterGroupSetOpenEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterGroupSetOpenEnum function


## -description


Starts the enumeration of groupset for a cluster.


## -parameters




### -param hCluster [in]

A handle to the cluster containing the groupset.


## -returns



If successful, returns a handle suitable for use with <a href="https://msdn.microsoft.com/926f67bd-2933-4b95-8320-166fe5299d7a">ClusterGroupSetEnum</a>


If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



