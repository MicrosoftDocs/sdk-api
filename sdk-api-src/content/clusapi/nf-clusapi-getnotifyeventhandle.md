---
UID: NF:clusapi.GetNotifyEventHandle
title: GetNotifyEventHandle function (clusapi.h)
description: Retrieves a handle to a notification event.
helpviewer_keywords: ["GetNotifyEventHandle","GetNotifyEventHandle function [Failover Cluster]","PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2","PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2 function [Failover Cluster]","clusapi/GetNotifyEventHandle","clusapi/PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2","mscs.getnotifyeventhandle"]
old-location: mscs\getnotifyeventhandle.htm
tech.root: MsCS
ms.assetid: DCA68080-B405-47E9-BC35-613EA56D1E59
ms.date: 12/05/2018
ms.keywords: GetNotifyEventHandle, GetNotifyEventHandle function [Failover Cluster], PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2, PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2 function [Failover Cluster], clusapi/GetNotifyEventHandle, clusapi/PCLUSAPI_GET_NOTIFY_EVENT_HANDLE_V2, mscs.getnotifyeventhandle
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNotifyEventHandle
 - clusapi/GetNotifyEventHandle
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
 - GetNotifyEventHandle
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

<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>