---
UID: NE:iketypes.IKEEXT_KEY_MODULE_TYPE_
title: IKEEXT_KEY_MODULE_TYPE (iketypes.h)
description: Specifies the type of keying module.
helpviewer_keywords: ["IKEEXT_KEY_MODULE_AUTHIP","IKEEXT_KEY_MODULE_IKE","IKEEXT_KEY_MODULE_IKEV2","IKEEXT_KEY_MODULE_MAX","IKEEXT_KEY_MODULE_TYPE","IKEEXT_KEY_MODULE_TYPE enumeration [Filtering]","fwp.ikeext_key_module_type","iketypes/IKEEXT_KEY_MODULE_AUTHIP","iketypes/IKEEXT_KEY_MODULE_IKE","iketypes/IKEEXT_KEY_MODULE_IKEV2","iketypes/IKEEXT_KEY_MODULE_MAX","iketypes/IKEEXT_KEY_MODULE_TYPE"]
old-location: fwp\ikeext_key_module_type.htm
tech.root: fwp
ms.assetid: a9268b07-343a-4a51-bc70-3e624facf617
ms.date: 12/05/2018
ms.keywords: IKEEXT_KEY_MODULE_AUTHIP, IKEEXT_KEY_MODULE_IKE, IKEEXT_KEY_MODULE_IKEV2, IKEEXT_KEY_MODULE_MAX, IKEEXT_KEY_MODULE_TYPE, IKEEXT_KEY_MODULE_TYPE enumeration [Filtering], fwp.ikeext_key_module_type, iketypes/IKEEXT_KEY_MODULE_AUTHIP, iketypes/IKEEXT_KEY_MODULE_IKE, iketypes/IKEEXT_KEY_MODULE_IKEV2, iketypes/IKEEXT_KEY_MODULE_MAX, iketypes/IKEEXT_KEY_MODULE_TYPE
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
req.typenames: IKEEXT_KEY_MODULE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_KEY_MODULE_TYPE_
 - iketypes/IKEEXT_KEY_MODULE_TYPE_
 - IKEEXT_KEY_MODULE_TYPE
 - iketypes/IKEEXT_KEY_MODULE_TYPE
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
 - IKEEXT_KEY_MODULE_TYPE
---

# IKEEXT_KEY_MODULE_TYPE enumeration


## -description

The <b>IKEEXT_KEY_MODULE_TYPE</b> enumerated type specifies the type of keying module.

## -enum-fields

### -field IKEEXT_KEY_MODULE_IKE:0

Specifies Internet Key Exchange (IKE) keying module.

### -field IKEEXT_KEY_MODULE_AUTHIP

Specifies Authenticated Internet Protocol (AuthIP) keying module.

### -field IKEEXT_KEY_MODULE_IKEV2

Specifies Internet Key Exchange version 2 (IKEv2) keying module.

Available only on Windows 7, Windows Server 2008 R2, and later.

### -field IKEEXT_KEY_MODULE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
