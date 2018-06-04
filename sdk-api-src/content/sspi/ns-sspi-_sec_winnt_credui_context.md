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

# _SEC_WINNT_CREDUI_CONTEXT structure


## -description


Specifies unserialized credential information. The credential information can be serialized by passing it as the <b>rgbSerialization</b> member of a <a href="_shell_credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure in a call to the <a href="_shell_icredentialprovider_setserialization">ICredentialProvider::SetSerialization</a> method.

The unserialized information can be obtained by calling the <a href="https://msdn.microsoft.com/c8861b27-d42d-4f7f-96c7-718f23fbaf86">SspiUnmarshalCredUIContext</a> function.


## -struct-fields




### -field cbHeaderLength

The size, in bytes, of the header.


### -field CredUIContextHandle

A handle to the credential context.


### -field UIInfo

A pointer to a <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure that specifies information for the credential prompt dialog box.


### -field dwAuthError

Specifies why prompting for credentials is needed. A caller can pass this Windows error parameter, returned by another authentication call, to allow the dialog box to accommodate certain errors. For example, if the password expired status code is passed, the dialog box prompts the user to change the password on the account.


### -field pInputAuthIdentity

The opaque authentication identity data.


### -field TargetName

The name of the target.

