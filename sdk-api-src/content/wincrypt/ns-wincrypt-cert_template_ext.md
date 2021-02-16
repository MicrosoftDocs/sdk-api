---
UID: NS:wincrypt._CERT_TEMPLATE_EXT
title: CERT_TEMPLATE_EXT (wincrypt.h)
description: A certificate template.
helpviewer_keywords: ["*PCERT_TEMPLATE_EXT","CERT_TEMPLATE_EXT","CERT_TEMPLATE_EXT structure [Security]","PCERT_TEMPLATE_EXT","PCERT_TEMPLATE_EXT structure pointer [Security]","_crypto2_cert_template_ext","security.cert_template_ext","wincrypt/CERT_TEMPLATE_EXT","wincrypt/PCERT_TEMPLATE_EXT"]
old-location: security\cert_template_ext.htm
tech.root: security
ms.assetid: 23cec38e-0d70-47bb-a2a4-6bbd3f4b018e
ms.date: 12/05/2018
ms.keywords: '*PCERT_TEMPLATE_EXT, CERT_TEMPLATE_EXT, CERT_TEMPLATE_EXT structure [Security], PCERT_TEMPLATE_EXT, PCERT_TEMPLATE_EXT structure pointer [Security], _crypto2_cert_template_ext, security.cert_template_ext, wincrypt/CERT_TEMPLATE_EXT, wincrypt/PCERT_TEMPLATE_EXT'
req.header: wincrypt.h
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
req.typenames: CERT_TEMPLATE_EXT, *PCERT_TEMPLATE_EXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_TEMPLATE_EXT
 - wincrypt/_CERT_TEMPLATE_EXT
 - PCERT_TEMPLATE_EXT
 - wincrypt/PCERT_TEMPLATE_EXT
 - CERT_TEMPLATE_EXT
 - wincrypt/CERT_TEMPLATE_EXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_TEMPLATE_EXT
---

# CERT_TEMPLATE_EXT structure


## -description

The <b>CERT_TEMPLATE_EXT</b> structure is a certificate template.

## -struct-fields

### -field pszObjId

<b>LPSTR</b> object identifier (OID).

### -field dwMajorVersion

<b>DWORD</b> indicating the major version of the template.

### -field fMinorVersion

<b>BOOL</b> flag set to <b>TRUE</b> if there is a minor version number.

### -field dwMinorVersion

<b>DWORD</b> indicating the minor version of the template.

