---
UID: NF:clusapi.RegisterClusterResourceTypeNotifyV2
title: RegisterClusterResourceTypeNotifyV2 function
author: windows-sdk-content
description: Adds a notification type to a cluster notification port.
old-location: mscs\registerclusterresourcetypenotifyv2.htm
tech.root: mscs
ms.assetid: 2E7DE3C3-F64B-4D5E-ADE9-B7CE60CB0E78
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegisterClusterResourceTypeNotifyV2, RegisterClusterResourceTypeNotifyV2 function [Failover Cluster], clusapi/RegisterClusterResourceTypeNotifyV2, mscs.registerclusterresourcetypenotifyv2
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
 - RegisterClusterResourceTypeNotifyV2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterClusterResourceTypeNotifyV2 function


## -description


Adds a notification type to a cluster notification port.This allows      an application to register for notification events that only affect a particular      cluster object.


## -parameters




### -param hChange [in]

A handle to the notification port.


### -param hCluster [in]

A handle to the cluster object.


### -param Flags [in]

A <a href="https://msdn.microsoft.com/2A49AA32-F1E2-4810-B093-F6EC050DA841">CLUSTER_CHANGE_RESOURCE_TYPE_V2</a> enumeration value that specifies the notification type to add.


### -param resTypeName [in]

A pointer to a null-terminated Unicode string that contains the name of the resource type.


### -param dwNotifyKey [in]

The notification key that is returned from the <a href="https://msdn.microsoft.com/0AF127E1-D517-4F4B-B797-40822B3B236F">GetClusterNotifyV2</a> function when the event occurs.


## -returns



<b>ERROR_SUCCESS</b> if the operation is successful; otherwise, a system error code.




## -see-also




<a href="https://msdn.microsoft.com/5bcb0411-d9c1-47e7-b799-5b1fcf2a9274">Resource Type Management Functions</a>
 

 

