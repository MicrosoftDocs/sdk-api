---
UID: NF:wcmconfig.ISettingsEngine.UnregisterNamespace
title: ISettingsEngine::UnregisterNamespace
author: windows-sdk-content
description: Unregisters an existing namespace.
old-location: smi\isettingsengine_unregisternamespace.htm
old-project: SMI
ms.assetid: c7254f87-fdf8-4b51-9a06-e593490cd3c5
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISettingsEngine interface [SMI],UnregisterNamespace method, ISettingsEngine.UnregisterNamespace, ISettingsEngine::UnregisterNamespace, UnregisterNamespace, UnregisterNamespace method [SMI], UnregisterNamespace method [SMI],ISettingsEngine interface, smi.isettingsengine_unregisternamespace, wcmconfig/ISettingsEngine::UnregisterNamespace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsEngine.UnregisterNamespace
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsEngine::UnregisterNamespace


## -description


Unregisters an existing namespace. This method is deprecated.


## -parameters




### -param SettingsID [in]

An <a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a> interface value that identifies the namespace to be unregistered.


### -param RemoveSettings [in]

When <b>true</b>, specifies that settings must be removed.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

