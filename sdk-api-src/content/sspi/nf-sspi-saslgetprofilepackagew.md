---
UID: NF:sspi.SaslGetProfilePackageW
title: SaslGetProfilePackageW function (sspi.h)
description: Returns the package information for the specified package. (Unicode)
helpviewer_keywords: ["SaslGetProfilePackage", "SaslGetProfilePackage function [Security]", "SaslGetProfilePackageW", "security.saslgetprofilepackage", "sspi/SaslGetProfilePackage", "sspi/SaslGetProfilePackageW"]
old-location: security\saslgetprofilepackage.htm
tech.root: security
ms.assetid: b7cecc5f-775f-40ba-abfc-27d51b3f5395
ms.date: 12/05/2018
ms.keywords: SaslGetProfilePackage, SaslGetProfilePackage function [Security], SaslGetProfilePackageA, SaslGetProfilePackageW, security.saslgetprofilepackage, sspi/SaslGetProfilePackage, sspi/SaslGetProfilePackageA, sspi/SaslGetProfilePackageW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaslGetProfilePackageW
 - sspi/SaslGetProfilePackageW
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
 - SaslGetProfilePackage
 - SaslGetProfilePackageA
 - SaslGetProfilePackageW
---

# SaslGetProfilePackageW function


## -description

The <b>SaslGetProfilePackage</b> function returns the package information for the specified package.

## -parameters

### -param ProfileName [in]

Unicode or ANSI string that contains the name of the SASL package.

### -param PackageInfo [out]

Pointer to a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure that returns the package information for the package specified by the <i>ProfileName</i> parameter.

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
Memory could not be allocated for the <a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The sspi.h header defines SaslGetProfilePackage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
