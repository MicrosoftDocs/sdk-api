---
UID: NF:shobjidl_core.ILaunchTargetMonitor.GetMonitor
title: ILaunchTargetMonitor::GetMonitor (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves the target monitor for the application being launched.
old-location: shell\ILaunchTargetMonitor_GetMonitor.htm
tech.root: shell
ms.assetid: 88437C86-DC0F-42F4-B58E-E732E1DAB9FD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMonitor, GetMonitor method [Windows Shell], GetMonitor method [Windows Shell],ILaunchTargetMonitor interface, ILaunchTargetMonitor interface [Windows Shell],GetMonitor method, ILaunchTargetMonitor.GetMonitor, ILaunchTargetMonitor::GetMonitor, shell.ILaunchTargetMonitor_GetMonitor, shobjidl_core/ILaunchTargetMonitor::GetMonitor
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ILaunchTargetMonitor.GetMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILaunchTargetMonitor::GetMonitor


## -description


Retrieves the target monitor for the application being launched.


## -parameters




### -param monitor [out]

Type: <b>HMONITOR*</b>

Contains the address of a pointer to the target  monitor's handle.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/358598D8-6488-4F8E-93CF-C70AD1A46862">ILaunchTargetMonitor</a>
 

 

