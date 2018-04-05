---
UID: NF:shobjidl_core.IPackageDebugSettings.EnumerateBackgroundTasks
title: IPackageDebugSettings::EnumerateBackgroundTasks method
author: windows-driver-content
description: Enumerates background tasks for the processes of the specified package.
old-location: winrt\ipackagedebugsettings_enumeratebackgroundtasks.htm
old-project: WinRT
ms.assetid: C86103F6-6893-483C-8237-CBBA71C784D2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EnumerateBackgroundTasks method [Windows Runtime], EnumerateBackgroundTasks method [Windows Runtime], IPackageDebugSettings interface, EnumerateBackgroundTasks,IPackageDebugSettings.EnumerateBackgroundTasks, IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], EnumerateBackgroundTasks method, IPackageDebugSettings::EnumerateBackgroundTasks, shobjidl_core/IPackageDebugSettings::EnumerateBackgroundTasks, winrt.ipackagedebugsettings_enumeratebackgroundtasks
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
-	IPackageDebugSettings.EnumerateBackgroundTasks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IPackageDebugSettings::EnumerateBackgroundTasks method


## -description


Enumerates background tasks for the processes of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


### -param taskCount [out]

Type: <b>ULONG*</b>

A pointer to a variable that receives the number of background tasks that were enumerated.


### -param taskIds [out]

Type: <b>LPCGUID*</b>

A pointer to memory space that receives a pointer to the array of IDs that represent all of the background tasks that were enumerated.


### -param taskNames [out]

Type: <b>LPCWSTR**</b>

A pointer to memory space that receives a pointer to the string of names for all of the background tasks that were enumerated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

