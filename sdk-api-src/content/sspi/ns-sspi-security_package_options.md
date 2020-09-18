---
UID: NS:sspi._SECURITY_PACKAGE_OPTIONS
title: SECURITY_PACKAGE_OPTIONS (sspi.h)
description: Specifies information about a security package.
helpviewer_keywords: ["*PSECURITY_PACKAGE_OPTIONS","PSECURITY_PACKAGE_OPTIONS","PSECURITY_PACKAGE_OPTIONS structure pointer [Security]","SECPKG_OPTIONS_TYPE_LSA","SECPKG_OPTIONS_TYPE_SSPI","SECPKG_OPTIONS_TYPE_UNKNOWN","SECURITY_PACKAGE_OPTIONS","SECURITY_PACKAGE_OPTIONS structure [Security]","security.security_package_options","sspi/PSECURITY_PACKAGE_OPTIONS","sspi/SECURITY_PACKAGE_OPTIONS"]
old-location: security\security_package_options.htm
tech.root: security
ms.assetid: 2e9f65ec-72a5-4d6f-aa63-f83369f0dd07
ms.date: 12/05/2018
ms.keywords: '*PSECURITY_PACKAGE_OPTIONS, PSECURITY_PACKAGE_OPTIONS, PSECURITY_PACKAGE_OPTIONS structure pointer [Security], SECPKG_OPTIONS_TYPE_LSA, SECPKG_OPTIONS_TYPE_SSPI, SECPKG_OPTIONS_TYPE_UNKNOWN, SECURITY_PACKAGE_OPTIONS, SECURITY_PACKAGE_OPTIONS structure [Security], security.security_package_options, sspi/PSECURITY_PACKAGE_OPTIONS, sspi/SECURITY_PACKAGE_OPTIONS'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SECURITY_PACKAGE_OPTIONS, *PSECURITY_PACKAGE_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_PACKAGE_OPTIONS
 - sspi/_SECURITY_PACKAGE_OPTIONS
 - PSECURITY_PACKAGE_OPTIONS
 - sspi/PSECURITY_PACKAGE_OPTIONS
 - SECURITY_PACKAGE_OPTIONS
 - sspi/SECURITY_PACKAGE_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SECURITY_PACKAGE_OPTIONS
---

# SECURITY_PACKAGE_OPTIONS structure


## -description

Specifies information about a security package. This structure is used by the <a href="/windows/desktop/api/sspi/nf-sspi-addsecuritypackagea">AddSecurityPackage</a> function.

## -struct-fields

### -field Size

The size, in bytes, of this structure.

### -field Type

The type of security package. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_OPTIONS_TYPE_UNKNOWN"></a><a id="secpkg_options_type_unknown"></a><dl>
<dt><b>SECPKG_OPTIONS_TYPE_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The package type is not known.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_OPTIONS_TYPE_LSA"></a><a id="secpkg_options_type_lsa"></a><dl>
<dt><b>SECPKG_OPTIONS_TYPE_LSA</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The security package is an <a href="/windows/desktop/SecAuthN/lsa-authentication">LSA authentication</a> package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_OPTIONS_TYPE_SSPI"></a><a id="secpkg_options_type_sspi"></a><dl>
<dt><b>SECPKG_OPTIONS_TYPE_SSPI</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The security package is a <a href="/windows/desktop/Rpc/security-support-provider-interface-sspi-">Security Support Provider Interface</a> (SSPI) package.

</td>
</tr>
</table>

### -field Flags

This member is reserved. Do not use it.

### -field SignatureSize

The size, in bytes, of a digital signature for this security package.

### -field Signature

A digital signature for this security package.