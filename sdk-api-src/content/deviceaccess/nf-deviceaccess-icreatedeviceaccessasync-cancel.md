---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Cancel
title: ICreateDeviceAccessAsync::Cancel method
author: windows-driver-content
description: The Cancel method attempts to cancel an asynchronous operation that is in progress.
old-location: deviceaccess\icreatedeviceaccessasync_cancel.htm
old-project: deviceaccess
ms.assetid: 06e5af2d-8bd8-44b1-9ead-caa362284530
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Cancel method [Device Access Broker API], Cancel method [Device Access Broker API], ICreateDeviceAccessAsync interface, Cancel,ICreateDeviceAccessAsync.Cancel, ICreateDeviceAccessAsync, ICreateDeviceAccessAsync interface [Device Access Broker API], Cancel method, ICreateDeviceAccessAsync::Cancel, deviceaccess.icreatedeviceaccessasync_cancel, deviceaccess/ICreateDeviceAccessAsync::Cancel
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
req.typenames: "*LPDDSURFACEDESC2, DDSURFACEDESC2"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Deviceaccess.lib
-	Deviceaccess.dll
api_name:
-	ICreateDeviceAccessAsync.Cancel
product: Windows
targetos: Windows
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
---

# ICreateDeviceAccessAsync::Cancel method


## -description


The <b>Cancel</b> method attempts to cancel an asynchronous operation that is in progress.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the operation is successfully canceled, a call to the <a href="https://msdn.microsoft.com/002e6638-a38a-4fda-b71c-a7a6983dda62">GetResult</a> method occurs.

Your application can call  <b>Cancel</b> at any time. If the operation is already closed or completed, it has no effect.




## -see-also




<a href="https://msdn.microsoft.com/ebc8d694-c933-4d98-95f5-67b0dd733d4d">ICreateDeviceAccessAsync</a>
 

 

