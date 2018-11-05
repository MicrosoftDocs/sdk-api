---
UID: NF:sspi.SspiEncodeStringsAsAuthIdentity
title: SspiEncodeStringsAsAuthIdentity function
author: windows-sdk-content
description: Encodes a set of three credential strings as an authentication identity structure.
old-location: security\sspiencodestringsasauthidentity.htm
tech.root: secauthn
ms.assetid: 0aea2f00-fcf1-4c4e-a22f-a669dd4fb294
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SspiEncodeStringsAsAuthIdentity, SspiEncodeStringsAsAuthIdentity function [Security], security.sspiencodestringsasauthidentity, sspi/SspiEncodeStringsAsAuthIdentity
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
 - SspiEncodeStringsAsAuthIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SspiEncodeStringsAsAuthIdentity function


## -description


Encodes a set of three credential strings as an authentication identity structure.


## -parameters




### -param pszUserName [in]

The user name associated with the identity to encode.


### -param pszDomainName [in]

The domain name associated with the identity to encode.


### -param pszPackedCredentialsString [in]

An encoded string version of a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure that specifies the user's credentials.


### -param ppAuthIdentity [out]

A pointer to the encoded identity structure.

When you have finished using this structure, free it by calling the <a href="https://msdn.microsoft.com/6199f66e-7adb-4bb9-8e77-a735e31dd5f6">SspiFreeAuthIdentity</a> function.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



