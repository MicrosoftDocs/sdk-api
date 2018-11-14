---
UID: NF:shobjidl_core.IPackageDebugSettings.TerminateAllProcesses
title: IPackageDebugSettings::TerminateAllProcesses
author: windows-sdk-content
description: Terminates all processes for the specified package.
old-location: shell\IPackageDebugSettings_TerminateAllProcesses.htm
tech.root: shell
ms.assetid: e49faeaa-8fd8-4233-94ac-0899177a9bb3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],TerminateAllProcesses method, IPackageDebugSettings.TerminateAllProcesses, IPackageDebugSettings::TerminateAllProcesses, TerminateAllProcesses, TerminateAllProcesses method [Windows Shell], TerminateAllProcesses method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_TerminateAllProcesses, shobjidl_core/IPackageDebugSettings::TerminateAllProcesses
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
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
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.TerminateAllProcesses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IPackageDebugSettings.TerminateAllProcesses
: 
---

# IPackageDebugSettings::TerminateAllProcesses


## -description


Terminates all processes for the specified package.


## -parameters




### -param packageFullName [in]

The package full name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not suspend the processes first. To test suspension followed by termination, call the <a href="https://msdn.microsoft.com/83f44285-46ed-4968-b0af-7964dfacf602">Suspend</a> method before calling <a href="https://msdn.microsoft.com/54be6d31-c9b9-41c6-a90f-31f6b9caef70">TerminateAllProcesses</a>.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

