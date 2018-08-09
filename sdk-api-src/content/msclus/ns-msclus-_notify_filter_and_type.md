---
UID: NS:msclus._NOTIFY_FILTER_AND_TYPE
title: "_NOTIFY_FILTER_AND_TYPE"
author: windows-sdk-content
description: Represents a filter for a notification port that was created by the CreateClusterNotifyPortV2 function. A filter specifies that a notification port accept notifications for the specified type of cluster object during the specified event.
old-location: mscs\notify_filter_and_type.htm
old-project: mscs
ms.assetid: E173F5D8-955B-44FF-980E-CEF536A87AF5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PNOTIFY_FILTER_AND_TYPE, NOTIFY_FILTER_AND_TYPE, NOTIFY_FILTER_AND_TYPE structure [Failover Cluster], PNOTIFY_FILTER_AND_TYPE, PNOTIFY_FILTER_AND_TYPE structure pointer [Failover Cluster], _NOTIFY_FILTER_AND_TYPE, _NOTIFY_FILTER_AND_TYPE structure [Failover Cluster], clusapi/NOTIFY_FILTER_AND_TYPE, clusapi/PNOTIFY_FILTER_AND_TYPE, clusapi/_NOTIFY_FILTER_AND_TYPE, msclus/NOTIFY_FILTER_AND_TYPE, msclus/PNOTIFY_FILTER_AND_TYPE, msclus/_NOTIFY_FILTER_AND_TYPE, mscs.notify_filter_and_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: NOTIFY_FILTER_AND_TYPE, *PNOTIFY_FILTER_AND_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _NOTIFY_FILTER_AND_TYPE structure


## -description


Represents a filter for a notification port that was created by the <a href="https://msdn.microsoft.com/81FE17A9-DE1C-4CDD-BE7D-50EA202D5AAC">CreateClusterNotifyPortV2</a> function. A filter specifies that  a   notification port accept  notifications for the specified type of cluster object during the specified event.


## -struct-fields




### -field dwObjectType

A <a href="https://msdn.microsoft.com/714C0EF1-7397-4227-B4B1-AFC5E61E08C2">CLUSTER_OBJECT_TYPE</a> enumeration value that specifies the cluster object type for the  filter.


### -field FilterFlags

A <a href="https://msdn.microsoft.com/EF414341-1EA4-4E69-AEA6-1CA3EAEAEDA5">CLUSTER_CHANGE_CLUSTER_V2</a> enumeration value that specifies the type for the filter.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

