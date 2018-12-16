---
UID: NF:ktmw32.SetResourceManagerCompletionPort
title: SetResourceManagerCompletionPort function
author: windows-sdk-content
description: Associates the specified I/O completion port with the specified resource manager (RM). This port receives all notifications for the RM.
old-location: fs\setresourcemanagercompletionport.htm
tech.root: ktm
ms.assetid: 219fc899-84ee-474f-9f86-6ebf9c721810
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetResourceManagerCompletionPort, SetResourceManagerCompletionPort function [Files], fs.setresourcemanagercompletionport, ktmw32/SetResourceManagerCompletionPort
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - SetResourceManagerCompletionPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetResourceManagerCompletionPort function


## -description


Associates the specified I/O completion port with the specified resource manager (RM). This port receives all notifications for the RM.


## -parameters




### -param ResourceManagerHandle [in]

A handle to the resource manager.


### -param IoCompletionPortHandle [in]

A handle to the I/O completion port.


### -param CompletionKey [in]

The user-defined identifier. Typically, it is used to associate the receive notification with a specific resource manager.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



This function must be used in conjunction with the <a href="https://msdn.microsoft.com/c83e104b-6cd7-4399-8232-7c2e7b408f1a">GetNotificationResourceManagerAsync</a> function, which provides the buffers that KTM uses to deliver notifications asynchronously. These functions provide a different way to receive notifications from KTM. You can use these two functions instead of the <a href="https://msdn.microsoft.com/d606f960-e843-4478-8ba7-5201f85c44ce">GetNotificationResourceManager</a> function.

This function must be called before calling <a href="https://msdn.microsoft.com/c83e104b-6cd7-4399-8232-7c2e7b408f1a">GetNotificationResourceManagerAsync</a>.




## -see-also




<a href="https://msdn.microsoft.com/d606f960-e843-4478-8ba7-5201f85c44ce">GetNotificationResourceManager</a>



<a href="https://msdn.microsoft.com/c83e104b-6cd7-4399-8232-7c2e7b408f1a">GetNotificationResourceManagerAsync</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

