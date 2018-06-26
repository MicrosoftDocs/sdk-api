---
UID: NF:shobjidl_core.IApplicationActivationManager.ActivateForProtocol
title: IApplicationActivationManager::ActivateForProtocol
author: windows-sdk-content
description: Activates the specified Windows Store app for the protocol contract (Windows.Protocol).
old-location: shell\IApplicationActivationManager_ActivateForProtocol.htm
old-project: shell
ms.assetid: A37E140A-5369-4abe-A9E9-8BD2E4492082
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: ActivateForProtocol, ActivateForProtocol method [Windows Shell], ActivateForProtocol method [Windows Shell],IApplicationActivationManager interface, IApplicationActivationManager interface [Windows Shell],ActivateForProtocol method, IApplicationActivationManager.ActivateForProtocol, IApplicationActivationManager::ActivateForProtocol, shell.IApplicationActivationManager_ActivateForProtocol, shobjidl_core/IApplicationActivationManager::ActivateForProtocol
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager.ActivateForProtocol
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IApplicationActivationManager::ActivateForProtocol


## -description


Activates the specified Windows Store app for the protocol contract (Windows.Protocol).


## -parameters




### -param appUserModelId [in]

The application user model ID of the Windows Store app.


### -param itemArray [in]

A pointer to an array of a single Shell item. The first item in the array is converted into a Uri object that is passed to the app through <a href="https://msdn.microsoft.com/03c9a412-01e3-49eb-b11c-a69156ed08a8">ProtocolActivatedEventArgs</a>. Any items in the array except for the first element are ignored.


### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfils this contract.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/66C8EDC8-AF05-46d6-B29D-B6EE09DF6709">IApplicationActivationManager</a>
 

 

