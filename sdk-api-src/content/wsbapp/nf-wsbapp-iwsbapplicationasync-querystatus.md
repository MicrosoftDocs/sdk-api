---
UID: NF:wsbapp.IWsbApplicationAsync.QueryStatus
title: IWsbApplicationAsync::QueryStatus
author: windows-sdk-content
description: Queries the status of an asynchronous operation.
old-location: wsb\iwsbapplicationasync_querystatus.htm
tech.root: wsb
ms.assetid: 0705e4a8-b65e-4740-b073-7fb24e5d02ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWsbApplicationAsync interface [Windows Server Backup],QueryStatus method, IWsbApplicationAsync.QueryStatus, IWsbApplicationAsync::QueryStatus, QueryStatus, QueryStatus method [Windows Server Backup], QueryStatus method [Windows Server Backup],IWsbApplicationAsync interface, S_OK, WSBAPP_ASYNC_IN_PROGRESS, wsb.iwsbapplicationasync_querystatus, wsbapp/IWsbApplicationAsync::QueryStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsbapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationAsync.QueryStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWsbApplicationAsync::QueryStatus


## -description


Queries the status of an asynchronous operation.


## -parameters




### -param phrResult [out]

The address of an <b>HRESULT</b> value that receives the status of the current asynchronous operation. If the asynchronous operation fails, this parameter receives the failure status code. Possible values include the following.



#### S_OK (0)

The asynchronous operation was completed successfully.



#### WSBAPP_ASYNC_IN_PROGRESS (0x407A0004L)

The asynchronous operation is still running.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Windows Server Backup calls this  method periodically to query the status of a pending asynchronous operation.




## -see-also




<a href="https://msdn.microsoft.com/cd8f74c0-c2dc-487c-b702-1e1355e99b7d">IWsbApplicationAsync</a>
 

 

