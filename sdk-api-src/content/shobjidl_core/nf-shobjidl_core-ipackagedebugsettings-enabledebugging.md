---
UID: NF:shobjidl_core.IPackageDebugSettings.EnableDebugging
title: IPackageDebugSettings::EnableDebugging
author: windows-sdk-content
description: Enables debug mode for the processes of the specified package.
old-location: shell\IPackageDebugSettings_EnableDebugging.htm
tech.root: shell
ms.assetid: a3afae41-b46e-47c8-95bb-a0aa747c6353
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: EnableDebugging, EnableDebugging method [Windows Shell], EnableDebugging method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],EnableDebugging method, IPackageDebugSettings.EnableDebugging, IPackageDebugSettings::EnableDebugging, shell.IPackageDebugSettings_EnableDebugging, shobjidl_core/IPackageDebugSettings::EnableDebugging
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
 - IPackageDebugSettings.EnableDebugging
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Enabling debug mode has the following effects:

<ul>
<li>Optionally enables debugger attach on activation.</li>
<li>Disables activation timeouts.</li>
<li>Disables automatic process suspension.</li>
<li>Disables automatic process termination.</li>
<li>Disables automatic process resumption.</li>
</ul>
To restore normal operation, call the <a href="https://msdn.microsoft.com/ad7efefb-aacd-48fa-bfe6-26271bd03b86">DisableDebugging</a> method.




## -see-also




<a href="https://msdn.microsoft.com/102e57be-296e-44ec-8211-f2c2d5eae1e6">DisableDebugging</a>



<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

