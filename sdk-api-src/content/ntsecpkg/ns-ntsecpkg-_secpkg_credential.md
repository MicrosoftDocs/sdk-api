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

# _SECPKG_CREDENTIAL structure


## -description


Specifies the credentials.


## -struct-fields




### -field Version

The version. 


### -field cbHeaderLength

The length of the header.


### -field cbStructureLength

The length of the structure, including the header, so that all of the content is in a contiguous buffer.


### -field ClientProcess

The identity of the client process.


### -field ClientThread

The identity of the client thread.


### -field LogonId

The logon identity of the caller.


### -field ClientToken

The client token of the caller.


### -field SessionId

The session identity of the caller.


### -field ModifiedId

The modified identity of the caller.


### -field fCredentials

The credentials that are passed in or returned.


### -field Flags

The credential flags.


### -field PrincipalName

Not currently used.


### -field PackageList

The list of packages. This member is only relevant to SPNego.


### -field MarshaledSuppliedCreds

The supplied credentials that are marshaled. This member contains a <a href="https://msdn.microsoft.com/23849312-7AC5-4D09-8889-27DFF8E32FE8">SECPKG_SUPPLIED_CREDENTIAL</a> 	structure.

