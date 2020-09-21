---
UID: NC:ntsecpkg.SpSetExtendedInformationFn
title: SpSetExtendedInformationFn (ntsecpkg.h)
description: Sets extended information about the security package.
helpviewer_keywords: ["SpSetExtendedInformation","SpSetExtendedInformation callback function [Security]","SpSetExtendedInformationFn","SpSetExtendedInformationFn callback","_ssp_spsetextendedinformation","ntsecpkg/SpSetExtendedInformation","security.spsetextendedinformation"]
old-location: security\spsetextendedinformation.htm
tech.root: security
ms.assetid: a6176786-c19b-4ecf-8a7b-2430ff8b56f7
ms.date: 12/05/2018
ms.keywords: SpSetExtendedInformation, SpSetExtendedInformation callback function [Security], SpSetExtendedInformationFn, SpSetExtendedInformationFn callback, _ssp_spsetextendedinformation, ntsecpkg/SpSetExtendedInformation, security.spsetextendedinformation
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
 - SpSetExtendedInformationFn
 - ntsecpkg/SpSetExtendedInformationFn
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
 - SpSetExtendedInformation
---

# SpSetExtendedInformationFn callback function


## -description

Sets extended information about the <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

## -parameters

### -param Class [in]

A 
<a href="/windows/win32/api/ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class">SECPKG_EXTENDED_INFORMATION_CLASS</a> enumeration value indicating the type of extended information.

### -param Info [in]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_extended_information">SECPKG_EXTENDED_INFORMATION</a> structure containing the extended information set.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

To retrieve extended information, the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> function is called.

An SSP/AP must implement the <b>SpSetExtendedInformation</b> function; however, the actual name given to the implementation is up to the package developer.

A pointer to the <b>SpSetExtendedInformation</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_extended_information">SECPKG_EXTENDED_INFORMATION</a>



<a href="/windows/win32/api/ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class">SECPKG_EXTENDED_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>