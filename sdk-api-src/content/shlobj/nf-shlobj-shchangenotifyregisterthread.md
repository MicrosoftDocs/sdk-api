---
UID: NF:shlobj.SHChangeNotifyRegisterThread
title: SHChangeNotifyRegisterThread function
author: windows-sdk-content
description: Enables asynchronous register and deregister of a thread.
old-location: shell\SHChangeNotifyRegisterThread.htm
old-project: shell
ms.assetid: 170afefc-b4de-4661-9c12-1341656b0fdb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHChangeNotifyRegisterThread, SHChangeNotifyRegisterThread function [Windows Shell], _shell_SHChangeNotifyRegisterThread, shell.SHChangeNotifyRegisterThread, shlobj/SHChangeNotifyRegisterThread
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# SHChangeNotifyRegisterThread function


## -description


Enables asynchronous register and deregister of a thread.


## -parameters




### -param status

Type: <b><a href="https://msdn.microsoft.com/31fd993b-d8cb-40cc-9f31-15711dba1b10">SCNRT_STATUS</a></b>

Indicates whether the function is being used to register or deregister the thread. One of the values of <a href="https://msdn.microsoft.com/31fd993b-d8cb-40cc-9f31-15711dba1b10">SCNRT_STATUS</a>.


## -returns



This function does not return a value.



