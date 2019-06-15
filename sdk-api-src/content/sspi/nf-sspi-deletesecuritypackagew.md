---
UID: NF:sspi.DeleteSecurityPackageW
title: DeleteSecurityPackageW function (sspi.h)
author: windows-sdk-content
description: Deletes a security support provider from the list of providers supported by Microsoft Negotiate.
old-location: security\deletesecuritypackage.htm
tech.root: SecAuthN
ms.assetid: 7a9a2c64-92a4-419b-8b20-d0f5cba64147
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteSecurityPackage, DeleteSecurityPackage function [Security], DeleteSecurityPackageA, DeleteSecurityPackageW, security.deletesecuritypackage, sspi/DeleteSecurityPackage, sspi/DeleteSecurityPackageA, sspi/DeleteSecurityPackageW
ms.topic: function
f1_keywords: ["sspi/DeleteSecurityPackage"]
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteSecurityPackageW (Unicode) and DeleteSecurityPackageA (ANSI)
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
 - DeleteSecurityPackage
 - DeleteSecurityPackageA
 - DeleteSecurityPackageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteSecurityPackageW function


## -description


Deletes a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security support provider</a> from the list of providers supported by <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a>.


## -parameters




### -param pszPackageName [in]

The name of the security provider to delete.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-addsecuritypackagea">AddSecurityPackage</a>
 

 

