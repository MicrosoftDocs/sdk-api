---
UID: NF:clusapi.ClusterGroupSetGetEnumCount
title: ClusterGroupSetGetEnumCount function (clusapi.h)
description: Gets the number of items contained the enumerator's collection.
helpviewer_keywords: ["ClusterGroupSetGetEnumCount","ClusterGroupSetGetEnumCount function [Failover Cluster]","clusapi/ClusterGroupSetGetEnumCount","mscs.clustergroupcollectiongetenumcount"]
old-location: mscs\clustergroupcollectiongetenumcount.htm
tech.root: MsCS
ms.assetid: 7e5f3b47-0f31-46eb-8e71-5bd1dc27190d
ms.date: 12/05/2018
ms.keywords: ClusterGroupSetGetEnumCount, ClusterGroupSetGetEnumCount function [Failover Cluster], clusapi/ClusterGroupSetGetEnumCount, mscs.clustergroupcollectiongetenumcount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterGroupSetGetEnumCount
 - clusapi/ClusterGroupSetGetEnumCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterGroupSetGetEnumCount
---

# ClusterGroupSetGetEnumCount function


## -description

Gets the number of items contained  the enumerator's collection.

## -parameters

### -param hGroupSetEnum [in]

A handle to an enumerator returned by <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clustergroupsetopenenum">ClusterGroupSetOpenEnum</a>.

## -returns

The number of items in the enumerator's collection. May be zero.