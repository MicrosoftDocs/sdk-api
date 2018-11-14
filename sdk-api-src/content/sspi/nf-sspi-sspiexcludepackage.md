---
UID: NF:sspi.SspiExcludePackage
title: SspiExcludePackage function
author: windows-sdk-content
description: Creates a new identity structure that is a copy of the specified identity structure modified to exclude the specified security support provider (SSP).
old-location: security\sspiexcludepackage.htm
tech.root: secauthn
ms.assetid: 2f85bb13-b72a-4c26-a328-9424a33a63b8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SspiExcludePackage, SspiExcludePackage function [Security], security.sspiexcludepackage, sspi/SspiExcludePackage
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
 - SspiExcludePackage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SspiExcludePackage
: 
---

# SspiExcludePackage function


## -description


Creates a new identity structure that is a copy of  the specified identity structure modified to exclude the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).


## -parameters




### -param AuthIdentity [in]

The identity structure to modify.


### -param pszPackageName [in]

The SSP to exclude.


### -param ppNewAuthIdentity [out]

The modified identity structure.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



