---
UID: NF:wnvapi.WnvOpen
title: WnvOpen function
author: windows-sdk-content
description: Provides a handle to the Windows Network Virtualization (WNV) driver object to be used to request and receive WNV notifications.
old-location: wnv\wnvopen.htm
old-project: wnv
ms.assetid: C20BA303-7ECD-4CF3-BB5E-D4509162CD85
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WnvOpen, WnvOpen function [Windows Network Virtualization], wnv.wnvopen, wnvapi/WnvOpen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WNV_OBJECT_TYPE, *PWNV_OBJECT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wnvapi.dll
api_name:
 - WnvOpen
product: Windows
targetos: Windows
req.lib: 
req.dll: Wnvapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WnvOpen function


## -description


Provides a handle to the Windows Network Virtualization (WNV) driver object to be used to request and receive WNV notifications.


## -parameters






## -returns



Type: <b>HANDLE</b>

If the function succeeds, it returns the handle to the WNV driver object. If the function fails, it returns <b>NULL</b>.




## -remarks



This handle is used for multiple invocations of the <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.



