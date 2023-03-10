---
UID: NS:iketypes.IKEEXT_CREDENTIAL0_
title: IKEEXT_CREDENTIAL0 (iketypes.h)
description: Is used to store credential information used for the authentication. (IKEEXT_CREDENTIAL0)
helpviewer_keywords: ["IKEEXT_CREDENTIAL0","IKEEXT_CREDENTIAL0 structure [Filtering]","fwp.ikeext_credential0","iketypes/IKEEXT_CREDENTIALS0"]
old-location: fwp\ikeext_credential0.htm
tech.root: fwp
ms.assetid: cb5aa4b6-71e7-43d4-a69c-4f209cd9755b
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIAL0, IKEEXT_CREDENTIAL0 structure [Filtering], fwp.ikeext_credential0, iketypes/IKEEXT_CREDENTIALS0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_CREDENTIAL0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CREDENTIAL0_
 - iketypes/IKEEXT_CREDENTIAL0_
 - IKEEXT_CREDENTIAL0
 - iketypes/IKEEXT_CREDENTIAL0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CREDENTIAL0
---

# IKEEXT_CREDENTIAL0 structure


## -description

The <b>IKEEXT_CREDENTIAL0</b> structure is  used to store credential information used for the authentication.
[IKEEXT_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential1) is available. For Windows 8, [IKEEXT_CREDENTIAL2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2) is available.</div><div> </div>

## -struct-fields

### -field authenticationMethodType

Type of authentication method.

See <a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a> for more information.

### -field impersonationType

Type of impersonation.

See <a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a> for more information.

### -field presharedKey

Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.

See <a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a> for more information.

### -field certificate

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_CERTIFICATE</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P256</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P384</b>
<b>IKEEXT_SSL</b>
<b>IKEEXT_SSL_ECDSA_P256</b>
<b>IKEEXT_SSL_ECDSA_P384</b>
<b>IKEEXT_IPV6_CGA</b>
See [IKEEXT_CERTIFICATE_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_credential0) for more information.

### -field name

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_KERBEROS</b>
<b>IKEEXT_NTML_V2</b>
See [IKEEXT_NAME_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_name_credential0) for more information.

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



[IKEEXT_CERTIFICATE_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_credential0)



[IKEEXT_NAME_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_name_credential0)



<a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
