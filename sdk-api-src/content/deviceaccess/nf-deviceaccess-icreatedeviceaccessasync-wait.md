---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Wait
title: ICreateDeviceAccessAsync::Wait method
author: windows-driver-content
description: The Wait method waits a specified length of time for an asynchronous bind operation that is in progress to finish.
old-location: deviceaccess\icreatedeviceaccessasync_wait.htm
old-project: deviceaccess
ms.assetid: 6fdab230-f8f7-47fa-838f-97316a4e78b9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ICreateDeviceAccessAsync, ICreateDeviceAccessAsync interface [Device Access Broker API], Wait method, ICreateDeviceAccessAsync::Wait, Wait method [Device Access Broker API], Wait method [Device Access Broker API], ICreateDeviceAccessAsync interface, Wait,ICreateDeviceAccessAsync.Wait, deviceaccess.icreatedeviceaccessasync_wait, deviceaccess/ICreateDeviceAccessAsync::Wait
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: deviceaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Deviceaccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIDEOMEMORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Deviceaccess.lib
-	Deviceaccess.dll
api_name:
-	ICreateDeviceAccessAsync.Wait
product: Windows
targetos: Windows
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
---

# ICreateDeviceAccessAsync::Wait method


## -description


The <b>Wait</b> method waits a specified length of time for an asynchronous bind operation that is in progress to finish.


## -parameters




### -param timeout [in]

Timeout value, in milliseconds, for the wait call. Use <b>INFINITE</b> if you want the caller to wait until the operation finishes.


## -returns



This method supports standard return values, in addition to these:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The wait was successful and the operation finished.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The wait timed out before the operation finished.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The operation has already closed when this method was called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ebc8d694-c933-4d98-95f5-67b0dd733d4d">ICreateDeviceAccessAsync</a>
 

 

