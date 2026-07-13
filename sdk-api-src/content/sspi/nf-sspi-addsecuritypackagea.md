---
UID: NF:sspi.AddSecurityPackageA
title: AddSecurityPackageA function (sspi.h)
description: Adds a security support provider to the list of providers supported by Microsoft Negotiate. (ANSI)
helpviewer_keywords: ["AddSecurityPackageA", "sspi/AddSecurityPackageA"]
old-location: security\addsecuritypackage.htm
tech.root: security
ms.assetid: 35b993d2-87a0-46d0-991f-88358b0cc5e6
ms.date: 12/05/2018
ms.keywords: AddSecurityPackage, AddSecurityPackage function [Security], AddSecurityPackageA, AddSecurityPackageW, security.addsecuritypackage, sspi/AddSecurityPackage, sspi/AddSecurityPackageA, sspi/AddSecurityPackageW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddSecurityPackageA
 - sspi/AddSecurityPackageA
dev_langs:
 - c++
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
---

# AddSecurityPackageA function


## -description

Adds a <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> to the list of providers supported by <a href="/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a>.

## -parameters

### -param pszPackageName [in]

The name of the package to add.

### -param pOptions [in]

A pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-security_package_options">SECURITY_PACKAGE_OPTIONS</a> structure that specifies additional information about the security package.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-deletesecuritypackagea">DeleteSecurityPackage</a>

## -remarks

> [!NOTE]
> The sspi.h header defines AddSecurityPackage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
