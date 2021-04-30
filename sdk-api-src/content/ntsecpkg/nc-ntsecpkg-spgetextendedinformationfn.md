---
UID: NC:ntsecpkg.SpGetExtendedInformationFn
title: SpGetExtendedInformationFn (ntsecpkg.h)
description: Provides extended information about a security package.
helpviewer_keywords: ["SpGetExtendedInformation","SpGetExtendedInformation callback function [Security]","SpGetExtendedInformationFn","SpGetExtendedInformationFn callback","_ssp_spgetextendedinformation","ntsecpkg/SpGetExtendedInformation","security.spgetextendedinformation"]
old-location: security\spgetextendedinformation.htm
tech.root: security
ms.assetid: e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3
ms.date: 12/05/2018
ms.keywords: SpGetExtendedInformation, SpGetExtendedInformation callback function [Security], SpGetExtendedInformationFn, SpGetExtendedInformationFn callback, _ssp_spgetextendedinformation, ntsecpkg/SpGetExtendedInformation, security.spgetextendedinformation
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpGetExtendedInformationFn
 - ntsecpkg/SpGetExtendedInformationFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpGetExtendedInformation
---

# SpGetExtendedInformationFn callback function


## -description

The <b>SpGetExtendedInformation</b> function provides extended information about a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

## -parameters

### -param Class [in]

A value from the 
<a href="/windows/win32/api/ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class">SECPKG_EXTENDED_INFORMATION_CLASS</a> enumeration indicating the type of extended information.

### -param ppInformation [out]

Pointer to a pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_extended_information">SECPKG_EXTENDED_INFORMATION</a> structure allocated by the security package. If the function call succeeds, the returned structure contains the requested information.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

Extended information is set using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> function.

An SSP/AP must implement the <b>SpGetExtendedInformation</b> function; however, the actual name given to the implementation is up to the package developer.

A pointer to the <b>SpGetExtendedInformation</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_extended_information">SECPKG_EXTENDED_INFORMATION</a>



<a href="/windows/win32/api/ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class">SECPKG_EXTENDED_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a>
