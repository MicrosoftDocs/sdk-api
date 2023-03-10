---
UID: NC:ntsecpkg.LSA_UPDATE_PRIMARY_CREDENTIALS
title: LSA_UPDATE_PRIMARY_CREDENTIALS (ntsecpkg.h)
description: Provides a mechanism for one security package to notify other packages that the credentials for a logon session have changed.
helpviewer_keywords: ["LSA_UPDATE_PRIMARY_CREDENTIALS","LSA_UPDATE_PRIMARY_CREDENTIALS callback","UpdateCredentials","UpdateCredentials callback function [Security]","_ssp_updatecredentials","ntsecpkg/UpdateCredentials","security.updatecredentials"]
old-location: security\updatecredentials.htm
tech.root: security
ms.assetid: 952ed682-775a-4370-8a89-15ca35553667
ms.date: 12/05/2018
ms.keywords: LSA_UPDATE_PRIMARY_CREDENTIALS, LSA_UPDATE_PRIMARY_CREDENTIALS callback, UpdateCredentials, UpdateCredentials callback function [Security], _ssp_updatecredentials, ntsecpkg/UpdateCredentials, security.updatecredentials
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
 - LSA_UPDATE_PRIMARY_CREDENTIALS
 - ntsecpkg/LSA_UPDATE_PRIMARY_CREDENTIALS
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
 - UpdateCredentials
---

# LSA_UPDATE_PRIMARY_CREDENTIALS callback function


## -description

Provides a mechanism for one <a href="/windows/desktop/SecGloss/s-gly">security package</a> to notify other packages that the <a href="/windows/desktop/SecGloss/c-gly">credentials</a> for a logon <a href="/windows/desktop/SecGloss/s-gly">session</a> have changed.

## -parameters

### -param PrimaryCredentials [in]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a> structure containing the <a href="/windows/desktop/SecGloss/p-gly">primary credentials</a>.

### -param Credentials [in, optional]

Optional. Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred_array">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a> structure containing the <a href="/windows/desktop/SecGloss/s-gly">supplemental credentials</a>.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.

## -remarks

To notify packages about the changed credentials, the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) calls the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptcredentialsfn">SpAcceptCredentials</a> function implementation in each package.

A pointer to the <b>UpdateCredentials</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred_array">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptcredentialsfn">SpAcceptCredentials</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>