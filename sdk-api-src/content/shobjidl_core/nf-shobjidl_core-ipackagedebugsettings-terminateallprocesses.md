---
UID: NF:shobjidl_core.IPackageDebugSettings.TerminateAllProcesses
title: IPackageDebugSettings::TerminateAllProcesses (shobjidl_core.h)
description: Terminates all processes for the specified package.
old-location: shell\IPackageDebugSettings_TerminateAllProcesses.htm
tech.root: shell
ms.assetid: e49faeaa-8fd8-4233-94ac-0899177a9bb3
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],TerminateAllProcesses method, IPackageDebugSettings.TerminateAllProcesses, IPackageDebugSettings::TerminateAllProcesses, TerminateAllProcesses, TerminateAllProcesses method [Windows Shell], TerminateAllProcesses method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_TerminateAllProcesses, shobjidl_core/IPackageDebugSettings::TerminateAllProcesses
f1_keywords:
- shobjidl_core/IPackageDebugSettings.TerminateAllProcesses
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This method does not suspend the processes first. To test suspension followed by termination, call the <a href="https://docs.microsoft.com/windows/desktop/WinRT/ipackagedebugsettings-suspend">Suspend</a> method before calling <a href="https://docs.microsoft.com/previous-versions/hh438399(v=vs.85)">TerminateAllProcesses</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>
 

 

