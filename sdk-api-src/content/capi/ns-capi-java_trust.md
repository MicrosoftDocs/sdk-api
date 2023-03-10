---
UID: NS:capi._JAVA_TRUST
title: JAVA_TRUST (capi.h)
description: Contains trust information.
helpviewer_keywords: ["*PJAVA_TRUST","JAVA_TRUST","JAVA_TRUST structure [Windows API]","PJAVA_TRUST","PJAVA_TRUST structure pointer [Windows API]","capi/JAVA_TRUST","capi/PJAVA_TRUST","winprog.java_trust"]
old-location: winprog\java_trust.htm
tech.root: winprog
ms.assetid: ceb8cfc4-3b29-47d1-a651-d3cee898c1eb
ms.date: 12/05/2018
ms.keywords: '*PJAVA_TRUST, JAVA_TRUST, JAVA_TRUST structure [Windows API], PJAVA_TRUST, PJAVA_TRUST structure pointer [Windows API], capi/JAVA_TRUST, capi/PJAVA_TRUST, winprog.java_trust'
req.header: capi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: JAVA_TRUST, *PJAVA_TRUST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JAVA_TRUST
 - capi/_JAVA_TRUST
 - PJAVA_TRUST
 - capi/PJAVA_TRUST
 - JAVA_TRUST
 - capi/JAVA_TRUST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Capi.h
api_name:
 - JAVA_TRUST
---

# JAVA_TRUST structure


## -description

Contains trust information.

## -struct-fields

### -field cbSize

The size of this structure, in bytes.

### -field flag

Reserved.

### -field fAllActiveXPermissions

Indicates whether all ActiveX permissions were requested.

### -field fAllPermissions

Indicates whether all Java permissions were requested.

### -field dwEncodingType

The encoding type. This member can be <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.

### -field pbJavaPermissions

The encoded permission blob.

### -field cbJavaPermissions

The size of the <b>pbJavaPermissions</b> buffer, in bytes.

### -field pbSigner

The encoded signer.

### -field cbSigner

The size of the <b>pbSigner</b> buffer, in bytes.

### -field pwszZone

The zone index.

### -field guidZone

Reserved.

### -field hVerify

The authenticode policy return code.

## -see-also

<a href="/windows/desktop/DevNotes/downloadjavaex">DownloadJavaEX</a>



<a href="/previous-versions/bb432350(v=vs.85)">JAVA_POLICY_PROVIDER</a>