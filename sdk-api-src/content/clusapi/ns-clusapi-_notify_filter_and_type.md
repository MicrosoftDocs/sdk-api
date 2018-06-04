---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

