---
UID: NF:roerrorapi.RoInspectThreadErrorInfo
title: RoInspectThreadErrorInfo function
author: windows-sdk-content
description: Gets the error object that represents the call stack at the point where the error originated.
old-location: winrt\roinspectthreaderrorinfo.htm
tech.root: WinRT
ms.assetid: DE7A930A-89CD-45C0-A232-800E5A5648F8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RoInspectThreadErrorInfo, RoInspectThreadErrorInfo function [Windows Runtime], roerrorapi/RoInspectThreadErrorInfo, winrt.roinspectthreaderrorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoInspectThreadErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RoInspectThreadErrorInfo function


## -description


Gets the error object that represents the call stack at the point where the error originated


## -parameters




### -param targetTebAddress [in]

The target thread environment block (TEB).


### -param machine

The machine to debug.


### -param readMemoryCallback

A callback function to read the buffer from the target TEB address space.


### -param context [in, optional]

Custom context data.


### -param targetErrorInfoAddress [out]

The address of the error object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the call to <b>RoInspectThreadErrorInfo</b> is  successful, <i>targetErrorInfoAddress</i> contains the address of an error object that you can pass to the <a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a> function to get the call stack at the point where the error was originated.




## -see-also




<a href="https://msdn.microsoft.com/A5BF207D-BB8D-47C1-8D32-0B6494809E2B">PINSPECT_MEMORY_CALLBACK</a>



<a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a>
 

 

