---
UID: NF:clusapi.GetNotifyEventHandle
title: GetNotifyEventHandle function
author: windows-driver-content
description: Retrieves a handle to a notification event.
old-location: mscs\getnotifyeventhandle.htm
old-project: MsCS
ms.assetid: DCA68080-B405-47E9-BC35-613EA56D1E59
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetNotifyEventHandle, GetNotifyEventHandle function [Failover Cluster], PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2, PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2 function [Failover Cluster], clusapi/GetNotifyEventHandle, clusapi/PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2, mscs.getnotifyeventhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
api_name:
-	GetNotifyEventHandle
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# GetNotifyEventHandle function


## -description


Retrieves a handle to a notification event.


## -parameters




### -param hChange [in]

A handle to the notification port that received the notification event.


### -param lphTargetEvent [out]

The handle to the notification event.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>. 

If the operation fails, the function returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 

