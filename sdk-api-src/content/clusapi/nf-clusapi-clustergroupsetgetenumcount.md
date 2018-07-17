---
UID: NF:clusapi.ClusterGroupSetGetEnumCount
title: ClusterGroupSetGetEnumCount function
author: windows-sdk-content
description: Gets the number of items contained the enumerator's collection.
old-location: mscs\clustergroupcollectiongetenumcount.htm
old-project: mscs
ms.assetid: 7e5f3b47-0f31-46eb-8e71-5bd1dc27190d
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusterGroupSetGetEnumCount, ClusterGroupSetGetEnumCount function [Failover Cluster], clusapi/ClusterGroupSetGetEnumCount, mscs.clustergroupcollectiongetenumcount
ms.prod: windows
ms.technology: windows-sdk
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
 - ClusterGroupSetGetEnumCount
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterGroupSetGetEnumCount function


## -description


Gets the number of items contained  the enumerator's collection.


## -parameters




### -param hGroupSetEnum [in]

A handle to an enumerator returned by <a href="https://msdn.microsoft.com/9e629cc8-2e5f-4682-a9b5-902d13a9792d">ClusterGroupSetOpenEnum</a>.


## -returns



The number of items in the enumerator's collection. May be zero.



