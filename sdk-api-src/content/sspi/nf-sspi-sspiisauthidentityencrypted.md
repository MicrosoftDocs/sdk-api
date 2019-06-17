---
UID: NF:sspi.SspiIsAuthIdentityEncrypted
title: SspiIsAuthIdentityEncrypted function (sspi.h)
author: windows-sdk-content
description: Indicates whether the specified identity structure is encrypted.
old-location: security\sspiisauthidentityencrypted.htm
tech.root: SecAuthN
ms.assetid: b85095f5-0ca5-4d75-866d-9b756404c1d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SspiIsAuthIdentityEncrypted, SspiIsAuthIdentityEncrypted function [Security], security.sspiisauthidentityencrypted, sspi/SspiIsAuthIdentityEncrypted
ms.topic: function
f1_keywords: ["sspi/SspiIsAuthIdentityEncrypted"]
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
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SspiIsAuthIdentityEncrypted function


## -description


Indicates whether the specified identity structure is encrypted.


## -parameters




### -param EncryptedAuthData [in]

The identity structure to test.


## -returns



<b>TRUE</b> if the identity structure specified by the <i>EncryptedAuthData</i> parameter is encrypted; otherwise, <b>FALSE</b>.



