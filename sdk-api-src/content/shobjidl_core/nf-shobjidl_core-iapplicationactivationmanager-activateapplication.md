---
UID: NF:shobjidl_core.IApplicationActivationManager.ActivateApplication
title: IApplicationActivationManager::ActivateApplication
author: windows-sdk-content
description: Activates the specified Windows Store app for the generic launch contract (Windows.Launch) in the current session.
old-location: shell\IApplicationActivationManager_ActivateApplication.htm
tech.root: shell
ms.assetid: A39FA68E-F79F-454a-BB41-31D4D5EEC253
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AO_DESIGNMODE, AO_NOERRORUI, AO_NONE, AO_NOSPLASHSCREEN, AO_PRELAUNCH, ActivateApplication, ActivateApplication method [Windows Shell], ActivateApplication method [Windows Shell],IApplicationActivationManager interface, IApplicationActivationManager interface [Windows Shell],ActivateApplication method, IApplicationActivationManager.ActivateApplication, IApplicationActivationManager::ActivateApplication, shell.IApplicationActivationManager_ActivateApplication, shobjidl_core/IApplicationActivationManager::ActivateApplication
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager.ActivateApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

