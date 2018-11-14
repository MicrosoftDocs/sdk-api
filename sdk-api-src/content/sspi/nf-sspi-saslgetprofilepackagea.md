---
UID: NF:sspi.SaslGetProfilePackageA
title: SaslGetProfilePackageA function
author: windows-sdk-content
description: Returns the package information for the specified package.
old-location: security\saslgetprofilepackage.htm
tech.root: secauthn
ms.assetid: b7cecc5f-775f-40ba-abfc-27d51b3f5395
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SaslGetProfilePackage, SaslGetProfilePackage function [Security], SaslGetProfilePackageA, SaslGetProfilePackageW, security.saslgetprofilepackage, sspi/SaslGetProfilePackage, sspi/SaslGetProfilePackageA, sspi/SaslGetProfilePackageW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SaslGetProfilePackageW (Unicode) and SaslGetProfilePackageA (ANSI)
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
 - SaslGetProfilePackage
 - SaslGetProfilePackageA
 - SaslGetProfilePackageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SaslGetProfilePackageA
: 
---

# SaslGetProfilePackageA function


## -description


The <b>SaslGetProfilePackage</b> function returns the package information for the specified package.


## -parameters




### -param ProfileName [in]

Unicode or ANSI string that contains the name of the SASL package.


### -param PackageInfo [out]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure that returns the package information for the package specified by the <i>ProfileName</i> parameter.


## -returns



If the call is completed successfully, this function returns SEC_E_OK. The following table shows some possible failure return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_SECPKG_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The SASL profile specified by the <i>ProfileName</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the <a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure.

</td>
</tr>
</table>
 



