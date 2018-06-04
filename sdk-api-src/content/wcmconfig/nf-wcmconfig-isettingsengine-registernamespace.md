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
 

 

