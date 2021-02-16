---
UID: NS:wincrypt._CERT_BIOMETRIC_DATA
title: CERT_BIOMETRIC_DATA (wincrypt.h)
description: Contains information about biometric data.
helpviewer_keywords: ["*PCERT_BIOMETRIC_DATA","CERT_BIOMETRIC_DATA","CERT_BIOMETRIC_DATA structure [Security]","CERT_BIOMETRIC_OID_DATA_CHOICE","CERT_BIOMETRIC_PICTURE_TYPE","CERT_BIOMETRIC_PREDEFINED_DATA_CHOICE","CERT_BIOMETRIC_SIGNATURE_TYPE","PCERT_BIOMETRIC_DATA","PCERT_BIOMETRIC_DATA structure pointer [Security]","security.cert_biometric_data","wincrypt/CERT_BIOMETRIC_DATA","wincrypt/PCERT_BIOMETRIC_DATA"]
old-location: security\cert_biometric_data.htm
tech.root: security
ms.assetid: 544297e2-b6a6-4a33-94b6-47066262506a
ms.date: 12/05/2018
ms.keywords: '*PCERT_BIOMETRIC_DATA, CERT_BIOMETRIC_DATA, CERT_BIOMETRIC_DATA structure [Security], CERT_BIOMETRIC_OID_DATA_CHOICE, CERT_BIOMETRIC_PICTURE_TYPE, CERT_BIOMETRIC_PREDEFINED_DATA_CHOICE, CERT_BIOMETRIC_SIGNATURE_TYPE, PCERT_BIOMETRIC_DATA, PCERT_BIOMETRIC_DATA structure pointer [Security], security.cert_biometric_data, wincrypt/CERT_BIOMETRIC_DATA, wincrypt/PCERT_BIOMETRIC_DATA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CERT_BIOMETRIC_DATA, *PCERT_BIOMETRIC_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_BIOMETRIC_DATA
 - wincrypt/_CERT_BIOMETRIC_DATA
 - PCERT_BIOMETRIC_DATA
 - wincrypt/PCERT_BIOMETRIC_DATA
 - CERT_BIOMETRIC_DATA
 - wincrypt/CERT_BIOMETRIC_DATA
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
 - CERT_BIOMETRIC_DATA
---

# CERT_BIOMETRIC_DATA structure


## -description

The <b>CERT_BIOMETRIC_DATA</b> structure contains information about biometric data.

## -struct-fields

### -field dwTypeOfBiometricDataChoice

Specifies the type of biometric data. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_BIOMETRIC_PREDEFINED_DATA_CHOICE"></a><a id="cert_biometric_predefined_data_choice"></a><dl>
<dt><b>CERT_BIOMETRIC_PREDEFINED_DATA_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The biometric data type is one of the predefined data types. The <b>dwPredefined</b> member specifies the data type.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_BIOMETRIC_OID_DATA_CHOICE"></a><a id="cert_biometric_oid_data_choice"></a><dl>
<dt><b>CERT_BIOMETRIC_OID_DATA_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The biometric data type is identified by the <b>pszObjId</b> member.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.dwPredefined

Specifies one of the predefined biometric data types. This member is only used if the <b>dwTypeOfBiometricDataChoice</b> member contains <b>CERT_BIOMETRIC_PREDEFINED_DATA_CHOICE</b>. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_BIOMETRIC_PICTURE_TYPE"></a><a id="cert_biometric_picture_type"></a><dl>
<dt><b>CERT_BIOMETRIC_PICTURE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The biometric data is a picture.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_BIOMETRIC_SIGNATURE_TYPE"></a><a id="cert_biometric_signature_type"></a><dl>
<dt><b>CERT_BIOMETRIC_SIGNATURE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The biometric data is a signature.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME.pszObjId

The address of a null-terminated ANSI string that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the biometric data type. This member is only used if the <b>dwTypeOfBiometricDataChoice</b> member contains <b>CERT_BIOMETRIC_OID_DATA_CHOICE</b>.

### -field HashedUrl

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a> structure that contains the hashed URL of the biometric data.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_biometric_ext_info">CERT_BIOMETRIC_EXT_INFO</a>