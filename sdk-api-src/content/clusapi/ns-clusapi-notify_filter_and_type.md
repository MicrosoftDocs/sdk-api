---
UID: NS:clusapi._NOTIFY_FILTER_AND_TYPE
title: NOTIFY_FILTER_AND_TYPE (clusapi.h)
description: Represents a filter for a notification port that was created by the CreateClusterNotifyPortV2 function. A filter specifies that a notification port accept notifications for the specified type of cluster object during the specified event.
helpviewer_keywords: ["*PNOTIFY_FILTER_AND_TYPE","NOTIFY_FILTER_AND_TYPE","NOTIFY_FILTER_AND_TYPE structure [Failover Cluster]","PNOTIFY_FILTER_AND_TYPE","PNOTIFY_FILTER_AND_TYPE structure pointer [Failover Cluster]","_NOTIFY_FILTER_AND_TYPE","_NOTIFY_FILTER_AND_TYPE structure [Failover Cluster]","clusapi/NOTIFY_FILTER_AND_TYPE","clusapi/PNOTIFY_FILTER_AND_TYPE","clusapi/_NOTIFY_FILTER_AND_TYPE","msclus/NOTIFY_FILTER_AND_TYPE","msclus/PNOTIFY_FILTER_AND_TYPE","msclus/_NOTIFY_FILTER_AND_TYPE","mscs.notify_filter_and_type"]
old-location: mscs\notify_filter_and_type.htm
tech.root: MsCS
ms.assetid: E173F5D8-955B-44FF-980E-CEF536A87AF5
ms.date: 12/05/2018
ms.keywords: '*PNOTIFY_FILTER_AND_TYPE, NOTIFY_FILTER_AND_TYPE, NOTIFY_FILTER_AND_TYPE structure [Failover Cluster], PNOTIFY_FILTER_AND_TYPE, PNOTIFY_FILTER_AND_TYPE structure pointer [Failover Cluster], _NOTIFY_FILTER_AND_TYPE, _NOTIFY_FILTER_AND_TYPE structure [Failover Cluster], clusapi/NOTIFY_FILTER_AND_TYPE, clusapi/PNOTIFY_FILTER_AND_TYPE, clusapi/_NOTIFY_FILTER_AND_TYPE, msclus/NOTIFY_FILTER_AND_TYPE, msclus/PNOTIFY_FILTER_AND_TYPE, msclus/_NOTIFY_FILTER_AND_TYPE, mscs.notify_filter_and_type'
f1_keywords:
- clusapi/NOTIFY_FILTER_AND_TYPE
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ClusApi.h
- MsClus.h
api_name:
- NOTIFY_FILTER_AND_TYPE
targetos: Windows
req.typenames: NOTIFY_FILTER_AND_TYPE, *PNOTIFY_FILTER_AND_TYPE
req.redist: 
ms.custom: 19H1
---

# NOTIFY_FILTER_AND_TYPE structure


## -description


Represents a filter for a notification port that was created by the <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyportv2">CreateClusterNotifyPortV2</a> function. A filter specifies that  a   notification port accept  notifications for the specified type of cluster object during the specified event.


## -struct-fields




### -field dwObjectType

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_object_type">CLUSTER_OBJECT_TYPE</a> enumeration value that specifies the cluster object type for the  filter.


### -field FilterFlags

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_change_cluster_v2">CLUSTER_CHANGE_CLUSTER_V2</a> enumeration value that specifies the type for the filter.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
 

 

