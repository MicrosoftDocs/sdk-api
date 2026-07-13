---
UID: NF:clusapi.CloseClusterNotifyPort
title: CloseClusterNotifyPort function (clusapi.h)
description: Closes a notification port established through CreateClusterNotifyPort.
helpviewer_keywords: ["CloseClusterNotifyPort","CloseClusterNotifyPort function [Failover Cluster]","PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT","PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT function [Failover Cluster]","_wolf_closeclusternotifyport","clusapi/CloseClusterNotifyPort","clusapi/PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT","mscs.closeclusternotifyport"]
old-location: mscs\closeclusternotifyport.htm
tech.root: MsCS
ms.assetid: abf7145c-780b-4ec7-babb-0e3975520f4a
ms.date: 12/05/2018
ms.keywords: CloseClusterNotifyPort, CloseClusterNotifyPort function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT, PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT function [Failover Cluster], _wolf_closeclusternotifyport, clusapi/CloseClusterNotifyPort, clusapi/PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT, mscs.closeclusternotifyport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CloseClusterNotifyPort
 - clusapi/CloseClusterNotifyPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - CloseClusterNotifyPort
---

# CloseClusterNotifyPort function


## -description

Closes a notification port established through  <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a>. The <b>PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT</b> type defines a pointer to this function.

## -parameters

### -param hChange [in]

Handle to the notification port to close.

## -returns

This function always returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-registerclusternotify">RegisterClusterNotify</a>