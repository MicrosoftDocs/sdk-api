---
UID: NS:ntsecapi._KERB_CHANGEPASSWORD_REQUEST
title: KERB_CHANGEPASSWORD_REQUEST
author: windows-sdk-content
description: Contains information used to change a password.
old-location: security\kerb_changepassword_request.htm
tech.root: secauthn
ms.assetid: 96463bac-0833-4a5e-b054-e32a29bc903d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PKERB_CHANGEPASSWORD_REQUEST, KERB_CHANGEPASSWORD_REQUEST, KERB_CHANGEPASSWORD_REQUEST structure [Security], PKERB_CHANGEPASSWORD_REQUEST, PKERB_CHANGEPASSWORD_REQUEST structure pointer [Security], ntsecapi/KERB_CHANGEPASSWORD_REQUEST, ntsecapi/PKERB_CHANGEPASSWORD_REQUEST, security.kerb_changepassword_request"
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_CHANGEPASSWORD_REQUEST
product: Windows
targetos: Windows
req.typenames: KERB_CHANGEPASSWORD_REQUEST, *PKERB_CHANGEPASSWORD_REQUEST
req.redist: 
---

# KERB_CHANGEPASSWORD_REQUEST structure


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

