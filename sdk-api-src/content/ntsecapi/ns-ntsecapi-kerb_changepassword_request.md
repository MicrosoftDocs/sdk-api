---
UID: NS:ntsecapi._KERB_CHANGEPASSWORD_REQUEST
title: KERB_CHANGEPASSWORD_REQUEST (ntsecapi.h)
description: Contains information used to change a password.
old-location: security\kerb_changepassword_request.htm
tech.root: SecAuthN
ms.assetid: 96463bac-0833-4a5e-b054-e32a29bc903d
ms.date: 12/05/2018
ms.keywords: '*PKERB_CHANGEPASSWORD_REQUEST, KERB_CHANGEPASSWORD_REQUEST, KERB_CHANGEPASSWORD_REQUEST structure [Security], PKERB_CHANGEPASSWORD_REQUEST, PKERB_CHANGEPASSWORD_REQUEST structure pointer [Security], ntsecapi/KERB_CHANGEPASSWORD_REQUEST, ntsecapi/PKERB_CHANGEPASSWORD_REQUEST, security.kerb_changepassword_request'
ms.topic: struct
f1_keywords:
- ntsecapi/KERB_CHANGEPASSWORD_REQUEST
dev_langs:
- c++
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
targetos: Windows
req.typenames: KERB_CHANGEPASSWORD_REQUEST, *PKERB_CHANGEPASSWORD_REQUEST
req.redist: 
ms.custom: 19H1
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

TRUE if the client is impersonating another <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security principal</a>. Otherwise, false.

