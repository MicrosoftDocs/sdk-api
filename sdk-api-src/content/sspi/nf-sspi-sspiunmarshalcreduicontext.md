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

# SspiUnmarshalCredUIContext function


## -description


Deserializes credential information obtained by a credential provider during  a previous call to the <a href="_shell_icredentialprovider_setserialization">ICredentialProvider::SetSerialization</a> method.


## -parameters




### -param MarshaledCredUIContext [in]

The serialized credential information obtained as the <b>rgbSerialization</b> member of the <a href="_shell_credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure retrieved from a call to the <a href="_shell_icredentialprovider_setserialization">ICredentialProvider::SetSerialization</a> method.


### -param MarshaledCredUIContextLength [in]

The size, in bytes, of the <i>MarshaledCredUIContext</i> buffer.


### -param CredUIContext [out]

A pointer to a <a href="https://msdn.microsoft.com/ac9410eb-ec1b-494c-8e8b-6d161ff2b41c">SEC_WINNT_CREDUI_CONTEXT</a> structure that specifies the deserialized credential information.


## -returns




                  If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



