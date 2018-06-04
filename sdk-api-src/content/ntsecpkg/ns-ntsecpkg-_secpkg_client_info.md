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

# _SECPKG_CLIENT_INFO structure


## -description


The <b>SECPKG_CLIENT_INFO</b> structure holds information about a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package's</a> client. This structure is used by the 
<a href="https://msdn.microsoft.com/3669f2e2-da70-4195-bdd0-f8415d97ae99">GetClientInfo</a> function.


## -struct-fields




### -field LogonId

The client's effective <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a>.


### -field ProcessID

The client's process identifier.


### -field ThreadID

The client's thread identifier.


### -field HasTcbPrivilege

<b>TRUE</b> if the client has the SeTcbPrivilege privilege; otherwise <b>FALSE</b>.


### -field Impersonating

<b>TRUE</b> if the client is impersonating another <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>.


### -field Restricted

The client is restricted in its ability to access securable objects or perform privileged operations.


### -field ClientFlags

 


### -field ImpersonationLevel

 


### -field ClientToken

 



