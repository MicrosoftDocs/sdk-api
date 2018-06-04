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

# IApplicationActivationManager::ActivateApplication


## -description


Activates the specified Windows Store app for the generic launch contract (Windows.Launch) in the current session.


## -parameters




### -param appUserModelId [in]

The application user model ID of the Windows Store app.


### -param arguments [in]

A pointer to an optional, app-specific, argument string.


### -param options [in]

One or more of the following flags used to support design mode, debugging, and testing scenarios.



#### AO_NONE (0x00000000)

No flags are set.



#### AO_DESIGNMODE (0x00000001)

The app is being activated for design mode, so it can't create its normal window. The creation of the app's window must be done by design tools that load the necessary components by communicating with a designer-specified service on the site chain established through the activation manager. Note that this means that the splash screen seen during regular activations won't be seen.

                                

Note that you must <a href="https://msdn.microsoft.com/a3afae41-b46e-47c8-95bb-a0aa747c6353">enable debug mode</a> on the app's package to succesfully use design mode.



#### AO_NOERRORUI (0x00000002)

Do not display an error dialog if the app fails to activate.



#### AO_NOSPLASHSCREEN (0x00000004)

Do not display the app's splash screen when the app is activated. You must <a href="https://msdn.microsoft.com/a3afae41-b46e-47c8-95bb-a0aa747c6353">enable debug mode</a> on the app's package when you use this flag; otherwise, the PLM will terminate the app after a few seconds.



#### AO_PRELAUNCH (0x2000000)

The application is being activated in prelaunch mode. This value is supported starting in Windows 10.


### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfils this contract.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/66C8EDC8-AF05-46d6-B29D-B6EE09DF6709">IApplicationActivationManager</a>



<a href="https://msdn.microsoft.com/a3afae41-b46e-47c8-95bb-a0aa747c6353">IPackageDebugSettings::EnableDebugging</a>
 

 

