---
UID: NF:shobjidl_core.IPackageDebugSettings.ActivateBackgroundTask
title: IPackageDebugSettings::ActivateBackgroundTask method
author: windows-driver-content
description: Activates the specified background task.
old-location: winrt\ipackagedebugsettings_activatebackgroundtask.htm
old-project: WinRT
ms.assetid: 5ACDAB41-5904-409B-86B2-96865B761868
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ActivateBackgroundTask method [Windows Runtime], ActivateBackgroundTask method [Windows Runtime], IPackageDebugSettings interface, ActivateBackgroundTask,IPackageDebugSettings.ActivateBackgroundTask, IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], ActivateBackgroundTask method, IPackageDebugSettings::ActivateBackgroundTask, shobjidl_core/IPackageDebugSettings::ActivateBackgroundTask, winrt.ipackagedebugsettings_activatebackgroundtask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OVERLAPPED, *LPOVERLAPPED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IPackageDebugSettings.ActivateBackgroundTask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IPackageDebugSettings::ActivateBackgroundTask method


## -description


Activates the specified background task.


## -parameters




### -param taskId [in]

Type: <b>LPCGUID</b>

The ID that represents the background task to activate.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

