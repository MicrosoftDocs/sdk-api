---
UID: NS:iketypes.IKEEXT_CREDENTIAL2_
title: IKEEXT_CREDENTIAL2 (iketypes.h)
description: Is used to store credential information used for the authentication. (IKEEXT_CREDENTIAL2)
helpviewer_keywords: ["IKEEXT_CREDENTIAL2","IKEEXT_CREDENTIAL2 structure [Filtering]","fwp.ikeext_credential2","iketypes/IKEEXT_CREDENTIAL2"]
old-location: fwp\ikeext_credential2.htm
tech.root: fwp
ms.assetid: b27689ef-5e2a-4163-a4d7-40f8939d4c66
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIAL2, IKEEXT_CREDENTIAL2 structure [Filtering], fwp.ikeext_credential2, iketypes/IKEEXT_CREDENTIAL2
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IKEEXT_CREDENTIAL2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CREDENTIAL2_
 - iketypes/IKEEXT_CREDENTIAL2_
 - IKEEXT_CREDENTIAL2
 - iketypes/IKEEXT_CREDENTIAL2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_CREDENTIAL2
---

# IKEEXT_CREDENTIAL2 structure


## -description

The <b>IKEEXT_CREDENTIAL2</b> structure is  used to store credential information used for the authentication.
[IKEEXT_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential1) is available. For Windows Vista, [IKEEXT_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential0)  is available.</div><div> </div>

## -struct-fields

### -field authenticationMethodType

Type: <b><a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a></b>

Type of authentication method.

### -field impersonationType

Type: <b><a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a></b>

Type of impersonation.

### -field presharedKey

Type: <b><a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a>*</b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.

### -field certificate

Type: [IKEEXT_CERTIFICATE_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_credential1)*</b>

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_CERTIFICATE</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P256</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P384</b>
<b>IKEEXT_SSL</b>
<b>IKEEXT_SSL_ECDSA_P256</b>
<b>IKEEXT_SSL_ECDSA_P384</b>
<b>IKEEXT_IPV6_CGA</b>

### -field name

Type: [IKEEXT_NAME_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_name_credential0)*</b>

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_KERBEROS</b>
<b>IKEEXT_NTML_V2</b>
<b>IKEEXT_RESERVED</b>

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



[IKEEXT_CERTIFICATE_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_credential1)



[IKEEXT_NAME_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_name_credential0)



<a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
