---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Close
title: ICreateDeviceAccessAsync::Close method
author: windows-driver-content
description: The Close method performs cleanup after the asynchronous operation is completed and you retrieve the results.
old-location: deviceaccess\icreatedeviceaccessasync_close.htm
old-project: deviceaccess
ms.assetid: 58887745-6a36-4600-9a1b-f9709a0e37e8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Close method [Device Access Broker API], Close method [Device Access Broker API], ICreateDeviceAccessAsync interface, Close,ICreateDeviceAccessAsync.Close, ICreateDeviceAccessAsync, ICreateDeviceAccessAsync interface [Device Access Broker API], Close method, ICreateDeviceAccessAsync::Close, deviceaccess.icreatedeviceaccessasync_close, deviceaccess/ICreateDeviceAccessAsync::Close
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
-	ICreateDeviceAccessAsync.Close
product: Windows
targetos: Windows
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
---

# ICreateDeviceAccessAsync::Close method


## -description


The <b>Close</b> method performs cleanup  after the asynchronous operation is completed and you retrieve the results.


## -parameters






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
The property value was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The operation did not finish.

</td>
</tr>
</table>
 




## -remarks



If the binding is successful, it doesn't invalidate the interface that the <a href="https://msdn.microsoft.com/002e6638-a38a-4fda-b71c-a7a6983dda62">GetResult</a> method returns.

It isn't strictly necessary to call this method, because resources are cleaned up when the underlying object is deleted. But doing so allows the system to free up resources that are associated with the asynchronous binding. As such, it's good practice to call <b>Close</b> after you retrieve the results.




## -see-also




<a href="https://msdn.microsoft.com/ebc8d694-c933-4d98-95f5-67b0dd733d4d">ICreateDeviceAccessAsync</a>
 

 

