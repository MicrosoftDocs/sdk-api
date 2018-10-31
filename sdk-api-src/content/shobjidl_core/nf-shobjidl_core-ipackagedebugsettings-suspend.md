---
UID: NF:shobjidl_core.IPackageDebugSettings.Suspend
title: IPackageDebugSettings::Suspend
author: windows-sdk-content
description: Suspends the processes of the package if they are currently running.
old-location: shell\IPackageDebugSettings_Suspend.htm
tech.root: shell
ms.assetid: b1a62712-cd03-4728-b0f1-c1b543f2e056
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],Suspend method, IPackageDebugSettings.Suspend, IPackageDebugSettings::Suspend, Suspend, Suspend method [Windows Shell], Suspend method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_Suspend, shobjidl_core/IPackageDebugSettings::Suspend
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
 - IPackageDebugSettings.Suspend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_STATECHANGE</b></dt>
</dl>
</td>
<td width="60%">
The process is not currently running.

</td>
</tr>
</table>
 




## -remarks



Each process receives the <a href="https://msdn.microsoft.com/29592ae4-6c38-4fb6-89d6-4d8d93c2e9d2">Suspending</a> event, which is useful for stepping through your apps as they respond to this event.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/2f0b3188-4c58-4ff6-983e-912131a7c934">Resume</a>
 

 

