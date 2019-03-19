---
UID: NS:sspi._SEC_WINNT_CREDUI_CONTEXT
title: SEC_WINNT_CREDUI_CONTEXT (sspi.h)
author: windows-sdk-content
description: Specifies unserialized credential information.
old-location: security\sec_winnt_credui_context.htm
tech.root: SecAuthN
ms.assetid: ac9410eb-ec1b-494c-8e8b-6d161ff2b41c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSEC_WINNT_CREDUI_CONTEXT, PSEC_WINNT_CREDUI_CONTEXT, PSEC_WINNT_CREDUI_CONTEXT structure pointer [Security], SEC_WINNT_CREDUI_CONTEXT, SEC_WINNT_CREDUI_CONTEXT structure [Security], security.sec_winnt_credui_context, sspi/PSEC_WINNT_CREDUI_CONTEXT, sspi/SEC_WINNT_CREDUI_CONTEXT"
ms.topic: struct
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Sspi.h
api_name:
 - SEC_WINNT_CREDUI_CONTEXT
product: Windows
targetos: Windows
req.typenames: SEC_WINNT_CREDUI_CONTEXT, *PSEC_WINNT_CREDUI_CONTEXT
req.redist: 
---

# SEC_WINNT_CREDUI_CONTEXT structure


## -description


Specifies unserialized credential information. The credential information can be serialized by passing it as the <b>rgbSerialization</b> member of a <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure in a call to the <a href="https://msdn.microsoft.com/en-us/library/Bb776043(v=VS.85).aspx">ICredentialProvider::SetSerialization</a> method.

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

