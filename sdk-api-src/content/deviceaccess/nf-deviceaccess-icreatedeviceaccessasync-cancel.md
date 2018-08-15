---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Cancel
title: ICreateDeviceAccessAsync::Cancel
author: windows-sdk-content
description: The Cancel method attempts to cancel an asynchronous operation that is in progress.
old-location: deviceaccess\icreatedeviceaccessasync_cancel.htm
old-project: deviceaccess
ms.assetid: 06e5af2d-8bd8-44b1-9ead-caa362284530
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Cancel, Cancel method [Device Access Broker API], Cancel method [Device Access Broker API],ICreateDeviceAccessAsync interface, ICreateDeviceAccessAsync interface [Device Access Broker API],Cancel method, ICreateDeviceAccessAsync.Cancel, ICreateDeviceAccessAsync::Cancel, deviceaccess.icreatedeviceaccessasync_cancel, deviceaccess/ICreateDeviceAccessAsync::Cancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: deviceaccess.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VIDEOMEMORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Deviceaccess.lib
 - Deviceaccess.dll
api_name:
 - ICreateDeviceAccessAsync.Cancel
product: Windows
targetos: Windows
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
---

# ICreateDeviceAccessAsync::Cancel


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
 

 

