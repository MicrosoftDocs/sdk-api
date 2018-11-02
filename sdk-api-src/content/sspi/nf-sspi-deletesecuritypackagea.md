---
UID: NF:sspi.DeleteSecurityPackageA
title: DeleteSecurityPackageA function
author: windows-sdk-content
description: Deletes a security support provider from the list of providers supported by Microsoft Negotiate.
old-location: security\deletesecuritypackage.htm
tech.root: secauthn
ms.assetid: 7a9a2c64-92a4-419b-8b20-d0f5cba64147
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DeleteSecurityPackage, DeleteSecurityPackage function [Security], DeleteSecurityPackageA, DeleteSecurityPackageW, security.deletesecuritypackage, sspi/DeleteSecurityPackage, sspi/DeleteSecurityPackageA, sspi/DeleteSecurityPackageW
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
---

# DeleteSecurityPackageA function


## -description


Deletes a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> from the list of providers supported by <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a>.


## -parameters




### -param pszPackageName [in]

The name of the security provider to delete.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.




## -see-also




<a href="https://msdn.microsoft.com/35b993d2-87a0-46d0-991f-88358b0cc5e6">AddSecurityPackage</a>
 

 

