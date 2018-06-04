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

# _KERB_CHANGEPASSWORD_REQUEST structure


## -description


The <b>KERB_CHANGEPASSWORD_REQUEST</b> structure contains information used to change a password.


## -struct-fields




### -field MessageType

 


### -field DomainName

<b>UNICODE_STRING</b> that contains the domain name of the account for which to change the password.


### -field AccountName

<b>UNICODE_STRING</b> that contains the account name of the account for which to change the password.


### -field OldPassword

<b>UNICODE_STRING</b> that contains the old password to be changed.


### -field NewPassword

<b>UNICODE_STRING</b> that contains the new password.


### -field Impersonating

TRUE if the client is impersonating another <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>. Otherwise, false.

