---
UID: NF:shobjidl_core.IPackageDebugSettings.EnableDebugging
title: IPackageDebugSettings::EnableDebugging (shobjidl_core.h)
description: Enables debug mode for the processes of the specified package.
helpviewer_keywords: ["EnableDebugging","EnableDebugging method [Windows Shell]","EnableDebugging method [Windows Shell]","IPackageDebugSettings interface","IPackageDebugSettings interface [Windows Shell]","EnableDebugging method","IPackageDebugSettings.EnableDebugging","IPackageDebugSettings::EnableDebugging","shell.IPackageDebugSettings_EnableDebugging","shobjidl_core/IPackageDebugSettings::EnableDebugging"]
old-location: shell\IPackageDebugSettings_EnableDebugging.htm
tech.root: shell
ms.assetid: a3afae41-b46e-47c8-95bb-a0aa747c6353
ms.date: 12/05/2018
ms.keywords: EnableDebugging, EnableDebugging method [Windows Shell], EnableDebugging method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],EnableDebugging method, IPackageDebugSettings.EnableDebugging, IPackageDebugSettings::EnableDebugging, shell.IPackageDebugSettings_EnableDebugging, shobjidl_core/IPackageDebugSettings::EnableDebugging
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
 - IPackageDebugSettings::EnableDebugging
 - shobjidl_core/IPackageDebugSettings::EnableDebugging
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
 - IPackageDebugSettings.EnableDebugging
---

# IPackageDebugSettings::EnableDebugging


## -description

Enables debug mode for the processes of the specified package.

## -parameters

### -param packageFullName [in]

The package full name.

### -param debuggerCommandLine [in]

The command line to use to launch processes from this package. This parameter is optional.

### -param environment [in]

Any environment strings to pass to processes. This parameter is optional.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Enabling debug mode has the following effects:

<ul>
<li>Optionally enables debugger attach on activation.</li>
<li>Disables activation timeouts.</li>
<li>Disables automatic process suspension.</li>
<li>Disables automatic process termination.</li>
<li>Disables automatic process resumption.</li>
</ul>
To restore normal operation, call the <a href="/previous-versions/hh438394(v=vs.85)">DisableDebugging</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-disabledebugging">DisableDebugging</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>