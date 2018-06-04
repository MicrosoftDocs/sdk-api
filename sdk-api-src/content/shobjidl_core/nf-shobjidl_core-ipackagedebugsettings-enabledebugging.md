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
 

 

