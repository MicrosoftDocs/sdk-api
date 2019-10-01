---
UID: NF:sspi.SspiPrepareForCredWrite
title: SspiPrepareForCredWrite function (sspi.h)
author: windows-sdk-content
description: Generates values from an identity structure that can be passed as the values of parameters in a call to the CredWrite function.
old-location: security\sspiprepareforcredwrite.htm
tech.root: SecAuthN
ms.assetid: 4db92042-38f2-42c2-9c94-b24e0eaafdf9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SspiPrepareForCredWrite, SspiPrepareForCredWrite function [Security], security.sspiprepareforcredwrite, sspi/SspiPrepareForCredWrite
ms.topic: function
f1_keywords: 
 - "sspi/SspiPrepareForCredWrite"
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
 - SspiPrepareForCredWrite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SspiPrepareForCredWrite function


## -description


Generates values from an identity structure that can be passed as the values of parameters in a call to the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> function.


## -parameters




### -param AuthIdentity [in]

The identity structure from which to generate the credentials to be passed to the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> function.


### -param pszTargetName [in]

A target name that can be modified by this function depending on the value of the <i>AuthIdentity</i> parameter.

Set the value of this parameter to <b>NULL</b> to use the user name as the target.


### -param pCredmanCredentialType [out]

The credential type to pass to the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> function.


### -param ppszCredmanTargetName [out]

The target name to pass to the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> function.


### -param ppszCredmanUserName [out]

The user name to pass to the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> function.


### -param ppCredentialBlob [out]

The credential <a href="https://docs.microsoft.com/windows/desktop/SecGloss/b-gly">BLOB</a> to send to the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> function.


### -param pCredentialBlobSize [out]

The size, in bytes, of the <i>ppCredentialBlob</i> buffer.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



