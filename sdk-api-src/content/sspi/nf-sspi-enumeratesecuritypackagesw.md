---
UID: NF:sspi.EnumerateSecurityPackagesW
title: EnumerateSecurityPackagesW function (sspi.h)
description: Returns an array of SecPkgInfo structures that provide information about the security packages available to the client. (Unicode)
helpviewer_keywords: ["EnumerateSecurityPackages", "EnumerateSecurityPackages function [Security]", "EnumerateSecurityPackagesW", "_ssp_enumeratesecuritypackages", "security.enumeratesecuritypackages", "sspi/EnumerateSecurityPackages", "sspi/EnumerateSecurityPackagesW"]
old-location: security\enumeratesecuritypackages.htm
tech.root: security
ms.assetid: 900790a6-111d-43f5-9316-e85aab03a3bc
ms.date: 12/05/2018
ms.keywords: EnumerateSecurityPackages, EnumerateSecurityPackages function [Security], EnumerateSecurityPackagesA, EnumerateSecurityPackagesW, _ssp_enumeratesecuritypackages, security.enumeratesecuritypackages, sspi/EnumerateSecurityPackages, sspi/EnumerateSecurityPackagesA, sspi/EnumerateSecurityPackagesW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumerateSecurityPackagesW (Unicode) and EnumerateSecurityPackagesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumerateSecurityPackagesW
 - sspi/EnumerateSecurityPackagesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - EnumerateSecurityPackages
 - EnumerateSecurityPackagesA
 - EnumerateSecurityPackagesW
---

# EnumerateSecurityPackagesW function


## -description

The <b>EnumerateSecurityPackages</b> function returns an array of 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structures that provide information about the <a href="/windows/desktop/SecGloss/s-gly">security packages</a> available to the client.

## -parameters

### -param pcPackages [in]

A pointer to a <b>ULONG</b> variable that receives the number of packages available on the system. This includes packages that are already loaded and packages available on demand.

### -param ppPackageInfo [in]

A pointer to a variable that receives a pointer to an array of 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structures. Each structure contains information from the <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP) that describes the capabilities of the security package available within that SSP.

When you have finished using the array, free the memory by calling the <a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.

## -returns

If the function succeeds, the function returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
<dt>0x80090300L</dt>
</dl>
</td>
<td width="60%">
There was not sufficient memory to allocate one or more of the buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE </b></dt>
<dt>0x80090301L</dt>
</dl>
</td>
<td width="60%">
An invalid handle was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_SECPKG_NOT_FOUND</b></dt>
<dt>0x80090305L</dt>
</dl>
</td>
<td width="60%">
The specified package was not found.

</td>
</tr>
</table>

## -remarks

The caller can use the <b>Name</b> member of a <a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure to specify a security package in a call to the 
<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (General)</a> function.





> [!NOTE]
> The sspi.h header defines EnumerateSecurityPackages as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (General)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a>
