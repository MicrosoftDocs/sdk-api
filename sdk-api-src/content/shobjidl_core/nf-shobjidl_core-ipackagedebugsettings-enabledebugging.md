---
UID: NF:shobjidl_core.IPackageDebugSettings.EnableDebugging
title: IPackageDebugSettings::EnableDebugging
author: windows-sdk-content
description: Enables debug mode for the processes of the specified package.
old-location: winrt\ipackagedebugsettings_enabledebugging.htm
tech.root: WinRT
ms.assetid: 6219e8d7-0631-482f-b602-b0453d4b1e70
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnableDebugging, EnableDebugging method [Windows Runtime], EnableDebugging method [Windows Runtime],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Runtime],EnableDebugging method, IPackageDebugSettings.EnableDebugging, IPackageDebugSettings::EnableDebugging, shobjidl_core/IPackageDebugSettings::EnableDebugging, winrt.ipackagedebugsettings_enabledebugging
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

Type: <b>LPCWSTR</b>

The package full name.


### -param debuggerCommandLine [in]

Type: <b>LPCWSTR</b>

The command line to use to launch processes from this package. This parameter is optional.


### -param environment [in]

Type: <b>PZZWSTR</b>

Any environment strings to pass to processes. This parameter is optional.


## -returns



Type: <b>HRESULT</b>

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




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

