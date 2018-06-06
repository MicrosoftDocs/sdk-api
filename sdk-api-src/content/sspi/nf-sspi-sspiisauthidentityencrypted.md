---
UID: NF:sspi.SspiIsAuthIdentityEncrypted
title: SspiIsAuthIdentityEncrypted function
author: windows-sdk-content
description: Indicates whether the specified identity structure is encrypted.
old-location: security\sspiisauthidentityencrypted.htm
old-project: SecAuthN
ms.assetid: b85095f5-0ca5-4d75-866d-9b756404c1d9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SspiIsAuthIdentityEncrypted, SspiIsAuthIdentityEncrypted function [Security], security.sspiisauthidentityencrypted, sspi/SspiIsAuthIdentityEncrypted
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
 - SspiIsAuthIdentityEncrypted
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiIsAuthIdentityEncrypted function


## -description


Indicates whether the specified identity structure is encrypted.


## -parameters




### -param EncryptedAuthData [in]

The identity structure to test.


## -returns



<b>TRUE</b> if the identity structure specified by the <i>EncryptedAuthData</i> parameter is encrypted; otherwise, <b>FALSE</b>.



