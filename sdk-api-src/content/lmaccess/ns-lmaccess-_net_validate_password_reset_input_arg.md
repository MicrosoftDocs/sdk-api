---
UID: NS:lmaccess._NET_VALIDATE_PASSWORD_RESET_INPUT_ARG
title: "_NET_VALIDATE_PASSWORD_RESET_INPUT_ARG"
author: windows-sdk-content
description: A client application passes the NET_VALIDATE_PASSWORD_RESET_INPUT_ARG structure to the NetValidatePasswordPolicy function when the application requests a password reset validation.
old-location: netmgmt\net_validate_password_reset_input_arg.htm
tech.root: netmgmt
ms.assetid: 3a6d4c2d-0d90-48bf-9dfa-2ba587538350
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PNET_VALIDATE_PASSWORD_RESET_INPUT_ARG, NET_VALIDATE_PASSWORD_RESET_INPUT_ARG, NET_VALIDATE_PASSWORD_RESET_INPUT_ARG structure [Network Management], PNET_VALIDATE_PASSWORD_RESET_INPUT_ARG, PNET_VALIDATE_PASSWORD_RESET_INPUT_ARG structure pointer [Network Management], _NET_VALIDATE_PASSWORD_RESET_INPUT_ARG, lmaccess/NET_VALIDATE_PASSWORD_RESET_INPUT_ARG, lmaccess/PNET_VALIDATE_PASSWORD_RESET_INPUT_ARG, netmgmt.net_validate_password_reset_input_arg"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - Lmaccess.h
api_name:
 - NET_VALIDATE_PASSWORD_RESET_INPUT_ARG
product: Windows
targetos: Windows
req.typenames: NET_VALIDATE_PASSWORD_RESET_INPUT_ARG, *PNET_VALIDATE_PASSWORD_RESET_INPUT_ARG
req.redist: 
---

# _NET_VALIDATE_PASSWORD_RESET_INPUT_ARG structure


## -description


A client application passes the <b>NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</b> structure to the <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> function when the application requests a password reset validation.


## -struct-fields




### -field InputPersistedFields

Specifies a <a href="https://msdn.microsoft.com/1e6ea28a-a007-4cd1-b5d6-686bcf019fa1">NET_VALIDATE_PERSISTED_FIELDS</a> structure that contains persistent password-related information about the account being logged on.


### -field ClearPassword

Pointer to a Unicode string specifying the new password, in plaintext format.


### -field UserAccountName

Pointer to a Unicode string specifying the name of the user account.


### -field HashedPassword

Specifies a <a href="https://msdn.microsoft.com/884e5b8c-1288-454e-862d-323d79123356">NET_VALIDATE_PASSWORD_HASH</a> structure that contains a hash of the new password.


### -field PasswordMustChangeAtNextLogon

BOOLEAN value that indicates whether the user must change his or her password at the next logon. If this parameter is <b>TRUE</b>, the user must change the password at the next logon.


### -field ClearLockout

BOOLEAN value that can reset the "lockout state" of the user account. If this member is <b>TRUE</b>,  the account will no longer be locked out.  Note that an application cannot directly lock out an account.  An account can be locked out only as a result of exceeding the maximum number of invalid password authentications allowed for the account.


## -see-also




<a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

