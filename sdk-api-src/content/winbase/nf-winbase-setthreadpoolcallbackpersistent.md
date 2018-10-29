---
UID: NF:winbase.SetThreadpoolCallbackPersistent
title: SetThreadpoolCallbackPersistent function
author: windows-sdk-content
description: Specifies that the callback should run on a persistent thread.
old-location: base\setthreadpoolcallbackpersistent.htm
tech.root: ProcThread
ms.assetid: 3f209586-5452-4928-8f97-70648b22460d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetThreadpoolCallbackPersistent, SetThreadpoolCallbackPersistent function, base.setthreadpoolcallbackpersistent, winbase/SetThreadpoolCallbackPersistent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - SetThreadpoolCallbackPersistent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadpoolCallbackPersistent function


## -description


Specifies that the callback should run on a persistent thread.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



This function is implemented as an inline function.

To compile an application that uses this function, set _WIN32_WINNT to _WIN32_WINNT_WIN7. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



