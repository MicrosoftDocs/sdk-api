---
UID: NF:sspi.EnumerateSecurityPackagesA
title: EnumerateSecurityPackagesA function
author: windows-sdk-content
description: Returns an array of SecPkgInfo structures that provide information about the security packages available to the client.
old-location: security\enumeratesecuritypackages.htm
tech.root: secauthn
ms.assetid: 900790a6-111d-43f5-9316-e85aab03a3bc
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: EnumerateSecurityPackages, EnumerateSecurityPackages function [Security], EnumerateSecurityPackagesA, EnumerateSecurityPackagesW, _ssp_enumeratesecuritypackages, security.enumeratesecuritypackages, sspi/EnumerateSecurityPackages, sspi/EnumerateSecurityPackagesA, sspi/EnumerateSecurityPackagesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumerateSecurityPackagesA function


## -description


The <b>EnumerateSecurityPackages</b> function returns an array of 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structures that provide information about the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a> available to the client.


## -parameters




### -param pcPackages [in]

A pointer to a <b>ULONG</b> variable that receives the number of packages available on the system. This includes packages that are already loaded and packages available on demand.


### -param ppPackageInfo [in]

A pointer to a variable that receives a pointer to an array of 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structures. Each structure contains information from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP) that describes the capabilities of the security package available within that SSP.

When you have finished using the array, free the memory by calling the <a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


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



The caller can use the <b>Name</b> member of a <a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure to specify a security package in a call to the 
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function.




## -see-also




<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="authentication_functions.htm">SSPI Functions</a>



<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a>
 

 

