---
UID: NF:sspi.SspiDecryptAuthIdentity
title: SspiDecryptAuthIdentity function
author: windows-sdk-content
description: Decrypts the specified encrypted credential.
old-location: security\sspidecryptauthidentity.htm
old-project: secauthn
ms.assetid: aef0206c-c376-4877-b1a6-5e86d2e35dea
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: SspiDecryptAuthIdentity, SspiDecryptAuthIdentity function [Security], security.sspidecryptauthidentity, sspi/SspiDecryptAuthIdentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - SspiDecryptAuthIdentity
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiDecryptAuthIdentity function


## -description


Decrypts the specified  encrypted credential.


## -parameters




### -param EncryptedAuthData [in, out]

On input, a  pointer to the encrypted credential structure to be decrypted. On output, a pointer to the decrypted credential structure.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



