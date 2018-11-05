---
UID: NF:sspi.AddSecurityPackageW
title: AddSecurityPackageW function
author: windows-sdk-content
description: Adds a security support provider to the list of providers supported by Microsoft Negotiate.
old-location: security\addsecuritypackage.htm
tech.root: secauthn
ms.assetid: 35b993d2-87a0-46d0-991f-88358b0cc5e6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AddSecurityPackage, AddSecurityPackage function [Security], AddSecurityPackageA, AddSecurityPackageW, security.addsecuritypackage, sspi/AddSecurityPackage, sspi/AddSecurityPackageA, sspi/AddSecurityPackageW
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
req.unicode-ansi: AddSecurityPackageW (Unicode) and AddSecurityPackageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - AddSecurityPackage
 - AddSecurityPackageA
 - AddSecurityPackageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddSecurityPackageW function


## -description


Adds a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> to the list of providers supported by <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a>.


## -parameters




### -param pszPackageName [in]

The name of the package to add.


### -param pOptions [in]

A pointer to a <a href="https://msdn.microsoft.com/2e9f65ec-72a5-4d6f-aa63-f83369f0dd07">SECURITY_PACKAGE_OPTIONS</a> structure that specifies additional information about the security package.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.




## -see-also




<a href="https://msdn.microsoft.com/7a9a2c64-92a4-419b-8b20-d0f5cba64147">DeleteSecurityPackage</a>
 

 

