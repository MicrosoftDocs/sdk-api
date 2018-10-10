---
UID: NF:shobjidl_core.IPackageDebugSettings.TerminateAllProcesses
title: IPackageDebugSettings::TerminateAllProcesses
author: windows-sdk-content
description: Terminates all processes for the specified package.
old-location: winrt\ipackagedebugsettings_terminateallprocesses.htm
tech.root: WinRT
ms.assetid: 54be6d31-c9b9-41c6-a90f-31f6b9caef70
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPackageDebugSettings interface [Windows Runtime],TerminateAllProcesses method, IPackageDebugSettings.TerminateAllProcesses, IPackageDebugSettings::TerminateAllProcesses, TerminateAllProcesses, TerminateAllProcesses method [Windows Runtime], TerminateAllProcesses method [Windows Runtime],IPackageDebugSettings interface, shobjidl_core/IPackageDebugSettings::TerminateAllProcesses, winrt.ipackagedebugsettings_terminateallprocesses
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
 - IPackageDebugSettings.TerminateAllProcesses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::TerminateAllProcesses


## -description


Terminates all processes for the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not suspend the processes first. To test suspension followed by termination, call the <a href="https://msdn.microsoft.com/83f44285-46ed-4968-b0af-7964dfacf602">Suspend</a> method before calling <b>TerminateAllProcesses</b>.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

