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

# _SEC_WINNT_AUTH_IDENTITY_W structure


## -description


The 
<b>SEC_WINNT_AUTH_IDENTITY</b> structure enables passing a particular user name and password to the run-time library for the purpose of authentication. The structure is valid for Windows and Macintosh.


## -struct-fields




### -field User

String containing the user name.


### -field UserLength

Number of characters in <b>User</b>, excluding the terminating <b>NULL</b>.


### -field Domain

String containing the domain  or workgroup name.


### -field DomainLength

Number of characters in <b>Domain</b>, excluding the terminating <b>NULL</b>.


### -field Password

String containing the user's password in the domain or workgroup.


### -field PasswordLength

Number of characters in <b>Password</b>, excluding the terminating <b>NULL</b>.


### -field Flags

Flags used to specify ANSI or UNICODE. Must be one of the following:

<a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a>
<a id="sec_winnt_auth_identity_ansi"></a>


#### SEC_WINNT_AUTH_IDENTITY_ANSI

<a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a>
<a id="sec_winnt_auth_identity_unicode"></a>


#### SEC_WINNT_AUTH_IDENTITY_UNICODE


##### - Flags.SEC_WINNT_AUTH_IDENTITY_ANSI

<a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a>
<a id="sec_winnt_auth_identity_unicode"></a>

##### - Flags.SEC_WINNT_AUTH_IDENTITY_UNICODE


## -remarks



This structure must remain valid for the lifetime of the binding handle unless pointed to from the <a href="https://msdn.microsoft.com/fdb7f42a-e545-4965-a44a-70d4631f1723">RPC_HTTP_TRANSPORT_CREDENTIALS</a> or <a href="https://msdn.microsoft.com/6f7c9ffe-2b21-48c0-98d5-16feacd50a20">RPC_HTTP_TRANSPORT_CREDENTIALS_V2</a> structure.

The strings may be ANSI or UNICODE depending on the value assigned to <b>Flags</b>.



