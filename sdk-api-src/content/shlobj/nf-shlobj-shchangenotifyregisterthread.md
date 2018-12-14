---
UID: NF:shlobj.SHChangeNotifyRegisterThread
title: SHChangeNotifyRegisterThread function
author: windows-sdk-content
description: Enables asynchronous register and deregister of a thread.
old-location: shell\SHChangeNotifyRegisterThread.htm
tech.root: shell
ms.assetid: 170afefc-b4de-4661-9c12-1341656b0fdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHChangeNotifyRegisterThread, SHChangeNotifyRegisterThread function [Windows Shell], _shell_SHChangeNotifyRegisterThread, shell.SHChangeNotifyRegisterThread, shlobj/SHChangeNotifyRegisterThread
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHChangeNotifyRegisterThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHChangeNotifyRegisterThread function


## -description


Enables asynchronous register and deregister of a thread.


## -parameters




### -param status

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762535(v=VS.85).aspx">SCNRT_STATUS</a></b>

Indicates whether the function is being used to register or deregister the thread. One of the values of <a href="https://msdn.microsoft.com/en-us/library/Bb762535(v=VS.85).aspx">SCNRT_STATUS</a>.


## -returns



This function does not return a value.



