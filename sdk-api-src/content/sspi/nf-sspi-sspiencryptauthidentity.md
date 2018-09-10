---
UID: NF:sspi.SspiEncryptAuthIdentity
title: SspiEncryptAuthIdentity function
author: windows-sdk-content
description: Encrypts the specified identity structure.
old-location: security\sspiencryptauthidentity.htm
tech.root: SecAuthN
ms.assetid: 4460f7ec-35fd-4ad1-8c20-dda9f4d3477a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SspiEncryptAuthIdentity, SspiEncryptAuthIdentity function [Security], security.sspiencryptauthidentity, sspi/SspiEncryptAuthIdentity
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SspiEncryptAuthIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SspiEncryptAuthIdentity function


## -description


Encrypts the specified identity structure.


## -parameters




### -param AuthData [in, out]

On input, the identity structure to encrypt. On output, the encrypted identity structure.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



