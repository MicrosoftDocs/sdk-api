---
UID: NF:sspi.SspiPrepareForCredRead
title: SspiPrepareForCredRead function
author: windows-sdk-content
description: Generates a target name and credential type from the specified identity structure.
old-location: security\sspiprepareforcredread.htm
tech.root: secauthn
ms.assetid: f473fd7a-5c0f-4a77-829b-28a82ad0d28d
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: SspiPrepareForCredRead, SspiPrepareForCredRead function [Security], security.sspiprepareforcredread, sspi/SspiPrepareForCredRead
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
 - SspiPrepareForCredRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SspiPrepareForCredRead function


## -description


Generates a target name and credential type from the specified identity structure.

The values that this function generates can be passed as the values of the <i>TargetName</i> and <i>Type</i> parameters in a call to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


## -parameters




### -param AuthIdentity [in]

The identity structure from which to generate the credentials to be passed to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


### -param pszTargetName [in]

A target name that can be modified by this function depending on the value of the <i>AuthIdentity</i> parameter.


### -param pCredmanCredentialType [out]

The credential type to pass to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


### -param ppszCredmanTargetName [out]

The target name to pass to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



