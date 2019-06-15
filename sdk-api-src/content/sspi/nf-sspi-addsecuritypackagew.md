---
UID: NF:sspi.AddSecurityPackageW
title: AddSecurityPackageW function (sspi.h)
author: windows-sdk-content
description: Adds a security support provider to the list of providers supported by Microsoft Negotiate.
old-location: security\addsecuritypackage.htm
tech.root: SecAuthN
ms.assetid: 35b993d2-87a0-46d0-991f-88358b0cc5e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddSecurityPackage, AddSecurityPackage function [Security], AddSecurityPackageA, AddSecurityPackageW, security.addsecuritypackage, sspi/AddSecurityPackage, sspi/AddSecurityPackageA, sspi/AddSecurityPackageW
ms.topic: function
f1_keywords: ["sspi/AddSecurityPackage"]
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
ms.custom: 19H1
---

# AddSecurityPackageW function


## -description


Adds a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security support provider</a> to the list of providers supported by <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a>.


## -parameters




### -param pszPackageName [in]

The name of the package to add.


### -param pOptions [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_security_package_options">SECURITY_PACKAGE_OPTIONS</a> structure that specifies additional information about the security package.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-deletesecuritypackagea">DeleteSecurityPackage</a>
 

 

