---
UID: NF:wcmconfig.ISettingsEngine.RegisterNamespace
title: ISettingsEngine::RegisterNamespace
author: windows-sdk-content
description: Registers a namespace from a stream.
old-location: smi\isettingsengine_registernamespace.htm
tech.root: SMI
ms.assetid: 9b9ffba8-b2b7-469e-96d2-78b086987fae
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISettingsEngine interface [SMI],RegisterNamespace method, ISettingsEngine.RegisterNamespace, ISettingsEngine::RegisterNamespace, RegisterNamespace, RegisterNamespace method [SMI], RegisterNamespace method [SMI],ISettingsEngine interface, smi.isettingsengine_registernamespace, wcmconfig/ISettingsEngine::RegisterNamespace
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
 - ISettingsEngine.RegisterNamespace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISettingsEngine::RegisterNamespace


## -description


Registers a namespace from a stream. The stream passed as a parameter to this method must be the XML for the configuration section of a manifest. This method is deprecated.


## -parameters




### -param SettingsID [in]

An <a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a> value that identifies the namespace to be registered.


### -param Stream [in]

The stream that specifies the configuration.


### -param PushSettings [in]

When this flag is set to <b>TRUE</b>, settings are pushed to the registry or to the initialization files. If the flag is not set, only the store for settings is changed.


### -param Results [out]

Results is a variant of type <b>VT_VARIANT</b> or <b>VT_ARRAY</b>, each of which points to an <a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a> object which describes an error or warning uncovered during manifest compilation.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

