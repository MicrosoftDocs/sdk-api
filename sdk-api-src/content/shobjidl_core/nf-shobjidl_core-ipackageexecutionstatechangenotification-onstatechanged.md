---
UID: NF:shobjidl_core.IPackageExecutionStateChangeNotification.OnStateChanged
title: IPackageExecutionStateChangeNotification::OnStateChanged
author: windows-sdk-content
description: Called when package state changes during Windows Store app debugging.
old-location: shell\IPackageExecutionStateChangeNotification_OnStateChanged.htm
tech.root: shell
ms.assetid: 254986AF-4572-4D63-B055-1C05A8FB0417
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IPackageExecutionStateChangeNotification interface [Windows Shell],OnStateChanged method, IPackageExecutionStateChangeNotification.OnStateChanged, IPackageExecutionStateChangeNotification::OnStateChanged, OnStateChanged, OnStateChanged method [Windows Shell], OnStateChanged method [Windows Shell],IPackageExecutionStateChangeNotification interface, shell.IPackageExecutionStateChangeNotification_OnStateChanged, shobjidl_core/IPackageExecutionStateChangeNotification::OnStateChanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IPackageExecutionStateChangeNotification.OnStateChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageExecutionStateChangeNotification::OnStateChanged


## -description


Called when package state changes during Windows Store app debugging.


## -parameters




### -param pszPackageFullName [in]

The package full name.


### -param pesNewState [in]

The new state that the package changed to.


## -returns



Return <b>S_OK</b> when you implement the <b>OnStateChanged</b>method. 




## -see-also




<a href="https://msdn.microsoft.com/6AD9A9CD-933B-432F-A124-48092588C5DF">IPackageExecutionStateChangeNotification</a>



<a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>
 

 

