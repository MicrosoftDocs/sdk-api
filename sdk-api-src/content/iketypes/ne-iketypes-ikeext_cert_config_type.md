---
UID: NE:iketypes.IKEEXT_CERT_CONFIG_TYPE_
title: IKEEXT_CERT_CONFIG_TYPE (iketypes.h)
description: Indicates a type of certificate configuration.
helpviewer_keywords: ["IKEEXT_CERT_CONFIG_ENTERPRISE_STORE","IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST","IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE","IKEEXT_CERT_CONFIG_TYPE","IKEEXT_CERT_CONFIG_TYPE enumeration [Filtering]","IKEEXT_CERT_CONFIG_TYPE_MAX","IKEEXT_CERT_CONFIG_UNSPECIFIED","fwp.ikeext_cert_config_type","iketypes/IKEEXT_CERT_CONFIG_ENTERPRISE_STORE","iketypes/IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST","iketypes/IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE","iketypes/IKEEXT_CERT_CONFIG_TYPE","iketypes/IKEEXT_CERT_CONFIG_TYPE_MAX","iketypes/IKEEXT_CERT_CONFIG_UNSPECIFIED"]
old-location: fwp\ikeext_cert_config_type.htm
tech.root: fwp
ms.assetid: b137e27b-c361-4fd2-9b3b-5c2b364576d4
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERT_CONFIG_ENTERPRISE_STORE, IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST, IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE, IKEEXT_CERT_CONFIG_TYPE, IKEEXT_CERT_CONFIG_TYPE enumeration [Filtering], IKEEXT_CERT_CONFIG_TYPE_MAX, IKEEXT_CERT_CONFIG_UNSPECIFIED, fwp.ikeext_cert_config_type, iketypes/IKEEXT_CERT_CONFIG_ENTERPRISE_STORE, iketypes/IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST, iketypes/IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE, iketypes/IKEEXT_CERT_CONFIG_TYPE, iketypes/IKEEXT_CERT_CONFIG_TYPE_MAX, iketypes/IKEEXT_CERT_CONFIG_UNSPECIFIED
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
req.typenames: IKEEXT_CERT_CONFIG_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERT_CONFIG_TYPE_
 - iketypes/IKEEXT_CERT_CONFIG_TYPE_
 - IKEEXT_CERT_CONFIG_TYPE
 - iketypes/IKEEXT_CERT_CONFIG_TYPE
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
 - IKEEXT_CERT_CONFIG_TYPE
---

# IKEEXT_CERT_CONFIG_TYPE enumeration


## -description

The <b>IKEEXT_CERT_CONFIG_TYPE</b> enumerated type indicates a type of certificate configuration.

## -enum-fields

### -field IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST:0

An explicit trust list will be used for authentication.

### -field IKEEXT_CERT_CONFIG_ENTERPRISE_STORE

The enterprise store will be used as the trust list for authentication.

### -field IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE

The trusted root CA store will be used as the trust list for authentication.

### -field IKEEXT_CERT_CONFIG_UNSPECIFIED

No certificate authentication in the direction (inbound or outbound) specified by the configuration.

Available only on Windows 7, Windows Server 2008 R2, and later.

### -field IKEEXT_CERT_CONFIG_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
