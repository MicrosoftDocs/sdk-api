---
UID: NF:wcmconfig.ISettingsEngine.GetNamespaces
title: ISettingsEngine::GetNamespaces
author: windows-sdk-content
description: Returns an enumerator to the installed namespaces.
old-location: smi\isettingsengine_getnamespaces.htm
tech.root: SMI
ms.assetid: 0beb20a5-3dbf-48c8-9b0c-aa3dd094b59d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetNamespaces, GetNamespaces method [SMI], GetNamespaces method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],GetNamespaces method, ISettingsEngine.GetNamespaces, ISettingsEngine::GetNamespaces, smi.isettingsengine_getnamespaces, wcmconfig/ISettingsEngine::GetNamespaces
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsEngine.GetNamespaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISettingsEngine::GetNamespaces


## -description


Returns an enumerator to the installed namespaces.


## -parameters




### -param Flags [in]

A <a href="https://msdn.microsoft.com/606fad95-1f93-4e16-9be5-2ebd52b91180">WcmNamespaceEnumerationFlags</a> value that specifies the context to include in the collection of namespaces.


### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param Namespaces [out]

An <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> interface pointer whose methods can be used to access members of the collection.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_USERNOTFOUND</b> if the store is not loaded.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

