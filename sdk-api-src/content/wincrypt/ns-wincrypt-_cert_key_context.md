---
UID: NS:wincrypt._CERT_KEY_CONTEXT
title: "_CERT_KEY_CONTEXT"
author: windows-driver-content
description: Contains data associated with a CERT_KEY_CONTEXT_PROP_ID property.
old-location: security\cert_key_context.htm
old-project: SecCrypto
ms.assetid: 796adb9c-ec38-41d0-8f8b-ea1053e9f9f0
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PCERT_KEY_CONTEXT, AT_KEYEXCHANGE, AT_SIGNATURE, CERT_KEY_CONTEXT, CERT_KEY_CONTEXT structure [Security], CERT_NCRYPT_KEY_SPEC, PCERT_KEY_CONTEXT, PCERT_KEY_CONTEXT structure pointer [Security], _CERT_KEY_CONTEXT, _crypto2_cert_key_context, security.cert_key_context, wincrypt/CERT_KEY_CONTEXT, wincrypt/PCERT_KEY_CONTEXT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CERT_KEY_CONTEXT, *PCERT_KEY_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_KEY_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_KEY_CONTEXT structure


## -description


The <b>CERT_KEY_CONTEXT</b> structure contains data associated with a CERT_KEY_CONTEXT_PROP_ID property.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hCryptProv

A <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) handle. This member is used when the <b>dwKeySpec</b> member contains <b>AT_KEYEXCHANGE</b> or <b>AT_SIGNATURE</b>.


### -field DUMMYUNIONNAME.hNCryptKey

A CNG CSP handle. This member is used when the <b>dwKeySpec</b> member contains <b>CERT_NCRYPT_KEY_SPEC</b>.

<b>Windows Server 2003 and Windows XP:  </b>This member is not available.


### -field dwKeySpec

The specification of the private key to retrieve. 




The following <b>dwKeySpec</b> values are defined for the default provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to encrypt/decrypt session keys.  The handle to the CSP is contained in the <b>hCryptProv</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to create and verify digital signatures.  The handle to the CSP is contained in the <b>hCryptProv</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NCRYPT_KEY_SPEC"></a><a id="cert_ncrypt_key_spec"></a><dl>
<dt><b>CERT_NCRYPT_KEY_SPEC</b></dt>
</dl>
</td>
<td width="60%">
Keys associated with a CNG CSP.  The handle to the CNG CSP is set in the <b>hNCryptProv</b> member.

<b>Windows Server 2003 and Windows XP:  </b>This value is not used.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>
 

 

