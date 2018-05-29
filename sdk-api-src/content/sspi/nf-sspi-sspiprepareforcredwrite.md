---
UID: NF:sspi.SspiPrepareForCredWrite
title: SspiPrepareForCredWrite function
author: windows-sdk-content
description: Generates values from an identity structure that can be passed as the values of parameters in a call to the CredWrite function.
old-location: security\sspiprepareforcredwrite.htm
old-project: SecAuthN
ms.assetid: 4db92042-38f2-42c2-9c94-b24e0eaafdf9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SspiPrepareForCredWrite, SspiPrepareForCredWrite function [Security], security.sspiprepareforcredwrite, sspi/SspiPrepareForCredWrite
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
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	SspiCli.dll
api_name:
-	SspiPrepareForCredWrite
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiPrepareForCredWrite function


## -description


Generates values from an identity structure that can be passed as the values of parameters in a call to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


## -parameters




### -param AuthIdentity [in]

The identity structure from which to generate the credentials to be passed to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param pszTargetName [in]

A target name that can be modified by this function depending on the value of the <i>AuthIdentity</i> parameter.

Set the value of this parameter to <b>NULL</b> to use the user name as the target.


### -param pCredmanCredentialType [out]

The credential type to pass to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param ppszCredmanTargetName [out]

The target name to pass to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param ppszCredmanUserName [out]

The user name to pass to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param ppCredentialBlob [out]

The credential <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> to send to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param pCredentialBlobSize [out]

The size, in bytes, of the <i>ppCredentialBlob</i> buffer.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



