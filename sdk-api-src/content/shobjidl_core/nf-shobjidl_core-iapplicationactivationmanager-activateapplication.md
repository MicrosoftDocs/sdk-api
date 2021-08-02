---
UID: NF:shobjidl_core.IApplicationActivationManager.ActivateApplication
title: IApplicationActivationManager::ActivateApplication (shobjidl_core.h)
description: Activates the specified Windows Store app for the generic launch contract (Windows.Launch) in the current session.
helpviewer_keywords: ["AO_DESIGNMODE","AO_NOERRORUI","AO_NONE","AO_NOSPLASHSCREEN","AO_PRELAUNCH","ActivateApplication","ActivateApplication method [Windows Shell]","ActivateApplication method [Windows Shell]","IApplicationActivationManager interface","IApplicationActivationManager interface [Windows Shell]","ActivateApplication method","IApplicationActivationManager.ActivateApplication","IApplicationActivationManager::ActivateApplication","shell.IApplicationActivationManager_ActivateApplication","shobjidl_core/IApplicationActivationManager::ActivateApplication"]
old-location: shell\IApplicationActivationManager_ActivateApplication.htm
tech.root: shell
ms.assetid: A39FA68E-F79F-454a-BB41-31D4D5EEC253
ms.date: 12/05/2018
ms.keywords: AO_DESIGNMODE, AO_NOERRORUI, AO_NONE, AO_NOSPLASHSCREEN, AO_PRELAUNCH, ActivateApplication, ActivateApplication method [Windows Shell], ActivateApplication method [Windows Shell],IApplicationActivationManager interface, IApplicationActivationManager interface [Windows Shell],ActivateApplication method, IApplicationActivationManager.ActivateApplication, IApplicationActivationManager::ActivateApplication, shell.IApplicationActivationManager_ActivateApplication, shobjidl_core/IApplicationActivationManager::ActivateApplication
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationActivationManager::ActivateApplication
 - shobjidl_core/IApplicationActivationManager::ActivateApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager.ActivateApplication
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

                                

Note that you must <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-enabledebugging">enable debug mode</a> on the app's package to successfully use design mode.



#### AO_NOERRORUI (0x00000002)

Do not display an error dialog if the app fails to activate.



#### AO_NOSPLASHSCREEN (0x00000004)

Do not display the app's splash screen when the app is activated. You must <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-enabledebugging">enable debug mode</a> on the app's package when you use this flag; otherwise, the PLM will terminate the app after a few seconds.



#### AO_PRELAUNCH (0x2000000)

The application is being activated in prelaunch mode. This value is supported starting in Windows 10.

### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfills this contract.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager">IApplicationActivationManager</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-enabledebugging">IPackageDebugSettings::EnableDebugging</a>