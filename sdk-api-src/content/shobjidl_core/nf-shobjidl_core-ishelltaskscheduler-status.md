---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IShellTaskScheduler::Status


## -description


Sets the release status and background thread timeout for the current task.


## -parameters




### -param dwReleaseStatus [in]

Type: <b>DWORD</b>

The following flag or 0.



#### ITSSFLAG_KILL_ON_DESTROY

Immediately cease execution of the current task when the <a href="https://msdn.microsoft.com/4898da7b-3d63-481f-a63a-d4f2554cfc8e">IShellTaskScheduler</a> instance is released.


### -param dwThreadTimeout [in]

Type: <b>DWORD</b>

Not used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



