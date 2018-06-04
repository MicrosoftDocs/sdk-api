---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _CERT_BIOMETRIC_DATA structure


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

The address of a null-terminated ANSI string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the biometric data type. This member is only used if the <b>dwTypeOfBiometricDataChoice</b> member contains <b>CERT_BIOMETRIC_OID_DATA_CHOICE</b>. 


### -field HashedUrl

A <a href="https://msdn.microsoft.com/961feb88-b924-4834-bc68-d87f410259f1">CERT_HASHED_URL</a> structure that contains the hashed URL of the biometric data.


## -see-also




<a href="https://msdn.microsoft.com/b2a877e1-2be2-428c-bc47-ec5ce6cef7e6">CERT_BIOMETRIC_EXT_INFO</a>
 

 

