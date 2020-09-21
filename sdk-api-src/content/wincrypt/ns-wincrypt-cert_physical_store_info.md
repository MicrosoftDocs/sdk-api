---
UID: NS:wincrypt._CERT_PHYSICAL_STORE_INFO
title: CERT_PHYSICAL_STORE_INFO (wincrypt.h)
description: Contains information on physical certificate stores.
helpviewer_keywords: ["*PCERT_PHYSICAL_STORE_INFO","CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG","CERT_PHYSICAL_STORE_INFO","CERT_PHYSICAL_STORE_INFO structure [Security]","CERT_PHYSICAL_STORE_INSERT_COMPUTER_NAME_ENABLE_FLAG","CERT_PHYSICAL_STORE_OPEN_DISABLE_FLAG","CERT_PHYSICAL_STORE_REMOTE_OPEN_DISABLE_FLAG","CERT_SYSTEM_STORE_RELOCATE_FLAG","PCERT_PHYSICAL_STORE_INFO","PCERT_PHYSICAL_STORE_INFO structure pointer [Security]","_crypto2_cert_physical_store_info","security.cert_physical_store_info","wincrypt/CERT_PHYSICAL_STORE_INFO","wincrypt/PCERT_PHYSICAL_STORE_INFO"]
old-location: security\cert_physical_store_info.htm
tech.root: security
ms.assetid: ad86f388-27af-442a-a76f-f386f66296ac
ms.date: 12/05/2018
ms.keywords: '*PCERT_PHYSICAL_STORE_INFO, CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG, CERT_PHYSICAL_STORE_INFO, CERT_PHYSICAL_STORE_INFO structure [Security], CERT_PHYSICAL_STORE_INSERT_COMPUTER_NAME_ENABLE_FLAG, CERT_PHYSICAL_STORE_OPEN_DISABLE_FLAG, CERT_PHYSICAL_STORE_REMOTE_OPEN_DISABLE_FLAG, CERT_SYSTEM_STORE_RELOCATE_FLAG, PCERT_PHYSICAL_STORE_INFO, PCERT_PHYSICAL_STORE_INFO structure pointer [Security], _crypto2_cert_physical_store_info, security.cert_physical_store_info, wincrypt/CERT_PHYSICAL_STORE_INFO, wincrypt/PCERT_PHYSICAL_STORE_INFO'
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
req.typenames: CERT_PHYSICAL_STORE_INFO, *PCERT_PHYSICAL_STORE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_PHYSICAL_STORE_INFO
 - wincrypt/_CERT_PHYSICAL_STORE_INFO
 - PCERT_PHYSICAL_STORE_INFO
 - wincrypt/PCERT_PHYSICAL_STORE_INFO
 - CERT_PHYSICAL_STORE_INFO
 - wincrypt/CERT_PHYSICAL_STORE_INFO
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
 - CERT_PHYSICAL_STORE_INFO
---

# CERT_PHYSICAL_STORE_INFO structure


## -description

The <b>CERT_PHYSICAL_STORE_INFO</b> structure contains information on physical <a href="/windows/desktop/SecGloss/c-gly">certificate stores</a>. Some members of these structures are passed directly to system calls of 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> to open the physical store.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pszOpenStoreProvider

A pointer to a string that names a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> provider type. This string is passed in a system call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> and determines the provider type of a certificate store to be opened. For the names of predefined certificate store types, see 
<b>CertOpenStore</b>. 




In addition to predefined certificate store provider types, new store provider types can be installed and registered with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress">CryptInstallOIDFunctionAddress</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidfunction">CryptRegisterOIDFunction</a>. For more information, see 
<a href="/windows/desktop/SecCrypto/extending-certopenstore-functionality">CertOpenStore</a>.

### -field dwOpenEncodingType

This member is applicable only when CERT_STORE_PROV_MSG, CERT_STORE_PROV_PKCS7, or CERT_STORE_PROV_FILENAME is passed in <i>lpszStoreProvider</i>. Otherwise, this member is not used. 




It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field dwOpenFlags

If a system store is opened with the SERVICES or USERS store location, the <b>dwOpenFlags</b> store location is set to CERT_SYSTEM_STORE_USERS or CERT_SYSTEM_STORE_SERVICES.

### -field OpenParameters

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> that contains data to be passed to the <i>pvPara</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function. The data type depends on the provider specified. For detailed information about the type and content to be passed, see descriptions of available providers in 
<b>CertOpenStore</b>.

### -field dwFlags

The following <b>dwFlags</b> values for CERT_PHYSICAL_STORE_INFO are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG"></a><a id="cert_physical_store_add_enable_flag"></a><dl>
<dt><b>CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Enables addition to a <a href="/windows/desktop/SecGloss/c-gly">context</a> to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PHYSICAL_STORE_OPEN_DISABLE_FLAG"></a><a id="cert_physical_store_open_disable_flag"></a><dl>
<dt><b>CERT_PHYSICAL_STORE_OPEN_DISABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Set by 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a> function. By default, all system stores located in the registry have an implicit SystemRegistry physical store that is opened. To disable the opening of this store, the SystemRegistry physical store that corresponds to the System store must be registered by setting CERT_PHYSICAL_STORE_OPEN_DISABLE_FLAG or by registering a physical store named ".Default" with 
<b>CertRegisterPhysicalStore</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PHYSICAL_STORE_REMOTE_OPEN_DISABLE_FLAG"></a><a id="cert_physical_store_remote_open_disable_flag"></a><dl>
<dt><b>CERT_PHYSICAL_STORE_REMOTE_OPEN_DISABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Disables remote opening of the physical store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PHYSICAL_STORE_INSERT_COMPUTER_NAME_ENABLE_FLAG"></a><a id="cert_physical_store_insert_computer_name_enable_flag"></a><dl>
<dt><b>CERT_PHYSICAL_STORE_INSERT_COMPUTER_NAME_ENABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Places the string \\ComputerName in front of other provider types.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_RELOCATE_FLAG"></a><a id="cert_system_store_relocate_flag"></a><dl>
<dt><b>CERT_SYSTEM_STORE_RELOCATE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Enables <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> to open a store relative to a user-specified HKEY instead of one of the predefined HKEY constants. For example, HKEY_CURRENT_USER can be replaced with a user-specified HKEY. When CERT_SYSTEM_STORE_RELOCATE_FLAG is set, the <i>pvPara</i> parameter passed to <b>CertOpenStore</b> points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure instead of pointing to the store name as a null-terminated <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> or <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> string.

</td>
</tr>
</table>

### -field dwPriority

When a system store is opened, its physical stores are ordered according to their <b>dwPriority</b> settings. A higher <b>dwPriority</b> indicates higher priority. The <b>dwPriority</b> member is passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress">CryptInstallOIDFunctionAddress</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidfunction">CryptRegisterOIDFunction</a>