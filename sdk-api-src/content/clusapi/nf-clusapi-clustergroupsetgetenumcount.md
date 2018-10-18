---
UID: NF:clusapi.ClusterGroupSetGetEnumCount
title: ClusterGroupSetGetEnumCount function
author: windows-sdk-content
description: Gets the number of items contained the enumerator's collection.
old-location: mscs\clustergroupcollectiongetenumcount.htm
tech.root: mscs
ms.assetid: 7e5f3b47-0f31-46eb-8e71-5bd1dc27190d
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ClusterGroupSetGetEnumCount, ClusterGroupSetGetEnumCount function [Failover Cluster], clusapi/ClusterGroupSetGetEnumCount, mscs.clustergroupcollectiongetenumcount
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
 - ClusterGroupSetGetEnumCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterGroupSetGetEnumCount function


## -description


Gets the number of items contained  the enumerator's collection.


## -parameters




### -param hGroupSetEnum [in]

A handle to an enumerator returned by <a href="https://msdn.microsoft.com/en-us/library/Mt705440(v=VS.85).aspx">ClusterGroupSetOpenEnum</a>.


## -returns



The number of items in the enumerator's collection. May be zero.



