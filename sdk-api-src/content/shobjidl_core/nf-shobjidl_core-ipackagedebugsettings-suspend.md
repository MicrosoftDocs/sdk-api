---
UID: NF:shobjidl_core.IPackageDebugSettings.Suspend
title: IPackageDebugSettings::Suspend (shobjidl_core.h)
description: Suspends the processes of the package if they are currently running.
helpviewer_keywords: ["IPackageDebugSettings interface [Windows Shell]","Suspend method","IPackageDebugSettings.Suspend","IPackageDebugSettings::Suspend","Suspend","Suspend method [Windows Shell]","Suspend method [Windows Shell]","IPackageDebugSettings interface","shell.IPackageDebugSettings_Suspend","shobjidl_core/IPackageDebugSettings::Suspend"]
old-location: shell\IPackageDebugSettings_Suspend.htm
tech.root: shell
ms.assetid: b1a62712-cd03-4728-b0f1-c1b543f2e056
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],Suspend method, IPackageDebugSettings.Suspend, IPackageDebugSettings::Suspend, Suspend, Suspend method [Windows Shell], Suspend method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_Suspend, shobjidl_core/IPackageDebugSettings::Suspend
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPackageDebugSettings::Suspend
 - shobjidl_core/IPackageDebugSettings::Suspend
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.Suspend
---

# IPackageDebugSettings::Suspend


## -description

Suspends the processes of the package if they are currently running.

## -parameters

### -param packageFullName [in]

The package full name.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The system has successfully started suspending the package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><em>A failing HRESULT value</em></dt>
</dl>
</td>
<td width="60%">
No process in the package is currently running, or another error occurred.

</td>
</tr>
</table>

## -remarks

Each process receives the <a href="/uwp/api/windows.applicationmodel.core.coreapplication.suspending">Suspending</a> event, which is useful for stepping through your apps as they respond to this event.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-resume">Resume</a>