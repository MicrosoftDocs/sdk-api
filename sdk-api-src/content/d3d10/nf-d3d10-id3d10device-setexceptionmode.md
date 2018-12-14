---
UID: NF:d3d10.ID3D10Device.SetExceptionMode
title: ID3D10Device::SetExceptionMode
author: windows-sdk-content
description: Get the exception-mode flags.
old-location: direct3d10\id3d10device_setexceptionmode.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setexceptionmode.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 450093c6-975d-3a2a-6e09-2d2267d36bae, ID3D10Device interface [Direct3D 10],SetExceptionMode method, ID3D10Device.SetExceptionMode, ID3D10Device::SetExceptionMode, SetExceptionMode, SetExceptionMode method [Direct3D 10], SetExceptionMode method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SetExceptionMode, direct3d10.id3d10device_setexceptionmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.SetExceptionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::SetExceptionMode


## -description


Get the exception-mode flags.


## -parameters




### -param RaiseFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="https://msdn.microsoft.com/en-us/library/Bb172407(v=VS.85).aspx">D3D10_RAISE_FLAG</a>. A default value of 0 means there are no flags.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



Set an exception-mode flag to elevate an error condition to a non-continuable exception. 

Whenever an error occurs, a Direct3D device enters the DEVICEREMOVED state and if the appropriate exception flag has been set, an exception is raised. A raised exception is designed to terminate an application. Before termination, the last chance an application has to persist data is by using an UnhandledExceptionFilter (see <a href="http://msdn2.microsoft.com/en-us/library/ms680657.aspx">Structured Exception Handling</a>). In general, UnhandledExceptionFilters are leveraged to try to persist data when an application is crashing (to disk, for example). Any code that executes during an UnhandledExceptionFilter is not guaranteed to reliably execute (due to possible process corruption). Any data that the UnhandledExceptionFilter manages to persist, before the UnhandledExceptionFilter crashes again, should be treated as suspect, and therefore inspected by a new, non-corrupted process to see if it is usable.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

