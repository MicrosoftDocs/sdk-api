---
UID: NF:wincrypt.CertOpenStore
title: CertOpenStore function (wincrypt.h)
description: Opens a certificate store by using a specified store provider type.
helpviewer_keywords: ["CERT_FILE_STORE_COMMIT_ENABLE","CERT_LDAP_STORE_AREC_EXCLUSIVE_FLAG","CERT_LDAP_STORE_OPENED_FLAG","CERT_LDAP_STORE_SIGN_FLAG","CERT_LDAP_STORE_UNBIND_FLAG","CERT_REGISTRY_STORE_REMOTE_FLAG","CERT_REGISTRY_STORE_SERIALIZED_FLAG","CERT_STORE_BACKUP_RESTORE_FLAG","CERT_STORE_CREATE_NEW_FLAG","CERT_STORE_DEFER_CLOSE_UNTIL_LAST_FREE_FLAG","CERT_STORE_DELETE_FLAG","CERT_STORE_ENUM_ARCHIVED_FLAG","CERT_STORE_MAXIMUM_ALLOWED_FLAG","CERT_STORE_NO_CRYPT_RELEASE_FLAG","CERT_STORE_OPEN_EXISTING_FLAG","CERT_STORE_PROV_COLLECTION","CERT_STORE_PROV_FILE","CERT_STORE_PROV_FILENAME(_W)","CERT_STORE_PROV_FILENAME_A","CERT_STORE_PROV_LDAP(_W)","CERT_STORE_PROV_MEMORY","CERT_STORE_PROV_MSG","CERT_STORE_PROV_PHYSICAL(_W)","CERT_STORE_PROV_PKCS12","CERT_STORE_PROV_PKCS7","CERT_STORE_PROV_REG","CERT_STORE_PROV_SERIALIZED","CERT_STORE_PROV_SMART_CARD(_W)","CERT_STORE_PROV_SYSTEM(_W)","CERT_STORE_PROV_SYSTEM_A","CERT_STORE_PROV_SYSTEM_REGISTRY(_W)","CERT_STORE_PROV_SYSTEM_REGISTRY_A","CERT_STORE_READONLY_FLAG","CERT_STORE_SET_LOCALIZED_NAME_FLAG","CERT_STORE_SHARE_CONTEXT_FLAG","CERT_STORE_UPDATE_KEYID_FLAG","CERT_SYSTEM_STORE_CURRENT_SERVICE","CERT_SYSTEM_STORE_CURRENT_USER","CERT_SYSTEM_STORE_CURRENT_USER_GROUP_POLICY","CERT_SYSTEM_STORE_LOCAL_MACHINE","CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE","CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY","CERT_SYSTEM_STORE_RELOCATE_FLAG","CERT_SYSTEM_STORE_SERVICES","CERT_SYSTEM_STORE_UNPROTECTED_FLAG","CERT_SYSTEM_STORE_USERS","CertOpenStore","CertOpenStore function [Security]","PKCS_7_ASN_ENCODING","X509_ASN_ENCODING","_crypto2_certopenstore","security.certopenstore","wincrypt/CertOpenStore"]
old-location: security\certopenstore.htm
tech.root: security
ms.assetid: 4edccbfe-c0a8-442b-b6b7-51ef598e7c90
ms.date: 12/05/2018
ms.keywords: CERT_FILE_STORE_COMMIT_ENABLE, CERT_LDAP_STORE_AREC_EXCLUSIVE_FLAG, CERT_LDAP_STORE_OPENED_FLAG, CERT_LDAP_STORE_SIGN_FLAG, CERT_LDAP_STORE_UNBIND_FLAG, CERT_REGISTRY_STORE_REMOTE_FLAG, CERT_REGISTRY_STORE_SERIALIZED_FLAG, CERT_STORE_BACKUP_RESTORE_FLAG, CERT_STORE_CREATE_NEW_FLAG, CERT_STORE_DEFER_CLOSE_UNTIL_LAST_FREE_FLAG, CERT_STORE_DELETE_FLAG, CERT_STORE_ENUM_ARCHIVED_FLAG, CERT_STORE_MAXIMUM_ALLOWED_FLAG, CERT_STORE_NO_CRYPT_RELEASE_FLAG, CERT_STORE_OPEN_EXISTING_FLAG, CERT_STORE_PROV_COLLECTION, CERT_STORE_PROV_FILE, CERT_STORE_PROV_FILENAME(_W), CERT_STORE_PROV_FILENAME_A, CERT_STORE_PROV_LDAP(_W), CERT_STORE_PROV_MEMORY, CERT_STORE_PROV_MSG, CERT_STORE_PROV_PHYSICAL(_W), CERT_STORE_PROV_PKCS12, CERT_STORE_PROV_PKCS7, CERT_STORE_PROV_REG, CERT_STORE_PROV_SERIALIZED, CERT_STORE_PROV_SMART_CARD(_W), CERT_STORE_PROV_SYSTEM(_W), CERT_STORE_PROV_SYSTEM_A, CERT_STORE_PROV_SYSTEM_REGISTRY(_W), CERT_STORE_PROV_SYSTEM_REGISTRY_A, CERT_STORE_READONLY_FLAG, CERT_STORE_SET_LOCALIZED_NAME_FLAG, CERT_STORE_SHARE_CONTEXT_FLAG, CERT_STORE_UPDATE_KEYID_FLAG, CERT_SYSTEM_STORE_CURRENT_SERVICE, CERT_SYSTEM_STORE_CURRENT_USER, CERT_SYSTEM_STORE_CURRENT_USER_GROUP_POLICY, CERT_SYSTEM_STORE_LOCAL_MACHINE, CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE, CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY, CERT_SYSTEM_STORE_RELOCATE_FLAG, CERT_SYSTEM_STORE_SERVICES, CERT_SYSTEM_STORE_UNPROTECTED_FLAG, CERT_SYSTEM_STORE_USERS, CertOpenStore, CertOpenStore function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, _crypto2_certopenstore, security.certopenstore, wincrypt/CertOpenStore
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertOpenStore
 - wincrypt/CertOpenStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertOpenStore
---

# CertOpenStore function


## -description

The <b>CertOpenStore</b> function opens a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> by using a specified store provider type. While this function can open a certificate store for most purposes, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a> is recommended to open the most common certificate stores. <b>CertOpenStore</b> is required for more complex options and special cases.

## -parameters

### -param lpszStoreProvider [in]

A pointer to a null-terminated ANSI string that contains the store provider type.

The following values  represent the predefined store types. The store provider type determines the contents of the <i>pvPara</i> parameter and the use and meaning of the high word of the <i>dwFlags</i> parameter. Additional store providers can be installed or registered by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress">CryptInstallOIDFunctionAddress</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidfunction">CryptRegisterOIDFunction</a> function. For more information about adding store providers, see 
<a href="/windows/desktop/SecCrypto/extending-certopenstore-functionality">Extending CertOpenStore Functionality</a>.





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_COLLECTION"></a><a id="cert_store_prov_collection"></a><dl>
<dt><b>CERT_STORE_PROV_COLLECTION</b></dt>
<dt><b>sz_CERT_STORE_PROV_COLLECTION</b></dt>
</dl>
</td>
<td width="60%">
Opens a store that will be a collection of other stores. Stores are added to or removed from the collection by using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certremovestorefromcollection">CertRemoveStoreFromCollection</a>. When a store is added to a collection, all certificates, CRLs, and CTLs in that store become available to searches or enumerations of the collection store.

The high word of <i>dwFlags</i> is set to zero.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter must be <b>NULL</b>.



</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FILE"></a><a id="cert_store_prov_file"></a><dl>
<dt><b>CERT_STORE_PROV_FILE</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs read from a specified open file. This provider expects the file to contain only a serialized store and not either PKCS #7 signed messages or a single encoded certificate.

The file pointer must be positioned at the beginning of the serialized store information. After the data in the serialized store has been loaded into the certificate store, the file pointer is positioned at the beginning of any data that can follow the serialized store data in the file. If CERT_FILE_STORE_COMMIT_ENABLE is set in <i>dwFlags</i>, the file handle is duplicated and the store is always committed as a serialized store. The file is not closed when the store is closed.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter must contain a pointer to the handle of a file opened by using <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.




</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FILENAME_A"></a><a id="cert_store_prov_filename_a"></a><dl>
<dt><b>CERT_STORE_PROV_FILENAME_A</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from a file. The provider opens the file and first attempts to read the file as a serialized store, then as a PKCS #7 signed message, and finally as a single encoded certificate.


The <i>dwEncodingType</i> parameter must contain the encoding types to be used with both messages and certificates. If the file contains an <a href="/windows/desktop/SecGloss/x-gly">X.509</a> encoded certificate, the open operation fails and a call to the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function will return <b>ERROR_ACCESS_DENIED</b>.
         If the <b>CERT_FILE_STORE_COMMIT_ENABLE</b> flag is set in <i>dwFlags</i>, the <i>dwCreationDisposition</i> value passed to <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> is as follows:

<ul>
<li>If the <b>CERT_STORE_CREATE_NEW_FLAG</b> flag is set, 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> uses <b>CREATE_NEW</b>.</li>
<li>If the <b>CERT_STORE_OPEN_EXISTING_FLAG</b> flag is set, <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> uses <b>OPEN_EXISTING</b>.</li>
<li>For all other settings of <i>dwFlags</i>, <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> uses <b>OPEN_ALWAYS</b>.</li>
</ul>


If <i>dwFlags</i> includes <b>CERT_FILE_STORE_COMMIT_ENABLE</b>, the file is committed as either a PKCS #7 or a serialized store depending on the file type opened. If the file was empty or if the file name has either a .p7c or .spc extension, the file is committed as a PKCS #7. Otherwise, the file is committed as a serialized store.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter must contain a pointer to null-terminated ANSI string that contains the name of an existing, unopened file.



</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FILENAME__W_"></a><a id="cert_store_prov_filename__w_"></a><dl>
<dt><b>CERT_STORE_PROV_FILENAME(_W)</b></dt>
<dt><b>sz_CERT_STORE_PROV_FILENAME(_W)</b></dt>
</dl>
</td>
<td width="60%">
Same as <b>CERT_STORE_PROV_FILENAME_A</b>.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter must contain a pointer to null-terminated Unicode string that contains the name of an existing, unopened file.



</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_LDAP__W_"></a><a id="cert_store_prov_ldap__w_"></a><dl>
<dt><b>CERT_STORE_PROV_LDAP(_W)</b></dt>
<dt><b>sz_CERT_STORE_PROV_LDAP(_W)</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from the results of an LDAP query.

To perform write operations on the store, the query string must specify a BASE query with no filter and a single attribute.

<b><i>pvPara</i> value:  </b>If the <i>dwFlags</i> parameter contains  <b>CERT_LDAP_STORE_OPENED_FLAG</b>, set  <i>pvPara</i> to the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_ldap_store_opened_para">CERT_LDAP_STORE_OPENED_PARA</a> structure that specifies the established LDAP session to use.

Otherwise,  set  <i>pvPara</i> to point to a null-terminated Unicode string that contains the LDAP query string. For more information about LDAP query strings, see <a href="/windows/desktop/ADSI/ldap-dialect">LDAP Dialect</a>.



</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_MEMORY"></a><a id="cert_store_prov_memory"></a><dl>
<dt><b>CERT_STORE_PROV_MEMORY</b></dt>
<dt><b>sz_CERT_STORE_PROV_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Creates a certificate store in cached memory. No certificates, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs), or <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs) are initially loaded into the store. Typically used to create a temporary store.

Any addition of certificates, CRLs, or CTLs or changes in properties of certificates, CRLs, or CTLs in a memory store are not automatically saved. They can be saved to a file or to a memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> by using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsavestore">CertSaveStore</a>.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_MSG"></a><a id="cert_store_prov_msg"></a><dl>
<dt><b>CERT_STORE_PROV_MSG</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from the specified cryptographic message. The <i>dwEncodingType</i> parameter must contain the encoding types used with both messages and certificates.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter contains an <b>HCRYPTMSG</b> handle of the encoded message, returned by a call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_PHYSICAL__W_"></a><a id="cert_store_prov_physical__w_"></a><dl>
<dt><b>CERT_STORE_PROV_PHYSICAL(_W)</b></dt>
<dt><b>sz_CERT_STORE_PROV_PHYSICAL(_W)</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from a specified physical store that is a member of a logical system store.

Two names are separated with an intervening backslash (\\), for example "Root\.Default". Here, "Root" is the name of the system store and ".Default" is the name of the physical store. The system and physical store names cannot contain any backslashes. The high word of <i>dwFlags</i> indicates the system store location, usually CERT_SYSTEM_STORE_CURRENT_USER. For more information, see <i>dwFlags</i> later in this topic and see <a href="/windows/desktop/SecCrypto/system-store-locations">System Store Locations</a>. Some physical store locations can be opened remotely.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a null-terminated Unicode string that contains both the system store name and physical names.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_PKCS7"></a><a id="cert_store_prov_pkcs7"></a><dl>
<dt><b>CERT_STORE_PROV_PKCS7</b></dt>
<dt><b>sz_CERT_STORE_PROV_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from an encoded PKCS #7 signed message. The <i>dwEncodingType</i> parameter must specify the encoding types to be used with both messages and certificates.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the encoded message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_PKCS12"></a><a id="cert_store_prov_pkcs12"></a><dl>
<dt><b>CERT_STORE_PROV_PKCS12</b></dt>
<dt><b>sz_CERT_STORE_PROV_PKCS12</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with the contents of a <a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a> packet.

If the PKCS #12 packet is protected with a NULL or empty password, this function will succeed in opening the store.

Beginning with Windows 8 and Windows Server 2012, if the password embedded in the PFX packet was protected to an Active Directory (AD) principal and the current user, as a member of that principal, has permission to decrypt the password, this function will succeed in opening the store. For more information, see the <i>pvPara</i> parameter and the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function.

You can protect PFX passwords to an AD principal beginning in Windows 8 and Windows Server 2012.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the PKCS #12 packet.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_REG"></a><a id="cert_store_prov_reg"></a><dl>
<dt><b>CERT_STORE_PROV_REG</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from a registry subkey.

This provider opens or creates the registry subkeys <b>Certificates</b>, <b>CRLs</b>, and <b>CTLs</b> under the key passed in <i>pvPara</i>. The input key is not closed by the provider. Before returning, the provider opens its own copy of the key passed in <i>pvPara</i>. If CERT_STORE_READONLY_FLAG is set in the low word of <i>dwFlags</i>, registry subkeys are opened by using the <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeya">RegOpenKey</a> with KEY_READ_ACCESS. Otherwise, registry subkeys are created by using <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeya">RegCreateKey</a> with KEY_ALL_ACCESS. Any changes to the contents of the opened store are immediately persisted to the registry. However, if CERT_STORE_READONLY_FLAG is set in the low word of <i>dwFlags</i>, any attempt to add to the contents of the store or to change a context's property results in an error with <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returning the E_ACCESSDENIED code.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter contains the handle of an open registry key.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SERIALIZED"></a><a id="cert_store_prov_serialized"></a><dl>
<dt><b>CERT_STORE_PROV_SERIALIZED</b></dt>
<dt><b>sz_CERT_STORE_PROV_SERIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from a memory location that contains a serialized store.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the serialized memory BLOB.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SMART_CARD__W_"></a><a id="cert_store_prov_smart_card__w_"></a><dl>
<dt><b>CERT_STORE_PROV_SMART_CARD(_W)</b></dt>
<dt><b>sz_CERT_STORE_PROV_SMART_CARD(_W)</b></dt>
</dl>
</td>
<td width="60%">
Not currently used.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SYSTEM_A"></a><a id="cert_store_prov_system_a"></a><dl>
<dt><b>CERT_STORE_PROV_SYSTEM_A</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from the specified system store.

The system store is a logical, collection store that consists of one or more physical stores. A physical store associated with a system store is registered with the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a> function. After the system store is opened, all of the physical stores that are associated with it are also opened by calls to <b>CertOpenStore</b> and are added to the system store collection by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a> function. The high word of <i>dwFlags</i> indicates the system store location, usually set to CERT_SYSTEM_STORE_CURRENT_USER. For details about registry locations, see <i>dwFlags</i> later in this topic and <a href="/windows/desktop/SecCrypto/system-store-locations">System Store Locations</a>. Some system store locations can be opened remotely; for more information, see System Store Locations.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a null-terminated ANSI string that contains a system store name, such as "My" or "Root".

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SYSTEM__W_"></a><a id="cert_store_prov_system__w_"></a><dl>
<dt><b>CERT_STORE_PROV_SYSTEM(_W)</b></dt>
<dt><b>sz_CERT_STORE_PROV_SYSTEM(_W)</b></dt>
</dl>
</td>
<td width="60%">
Same as <b>CERT_STORE_PROV_SYSTEM_A</b>.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a null-terminated Unicode string that contains a system store name, such as "My" or "Root".

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SYSTEM_REGISTRY_A"></a><a id="cert_store_prov_system_registry_a"></a><dl>
<dt><b>CERT_STORE_PROV_SYSTEM_REGISTRY_A</b></dt>
</dl>
</td>
<td width="60%">
Initializes the store with certificates, CRLs, and CTLs from a physical registry store. The physical store is not opened as a collection store. Enumerations and searches go through only the certificates, CRLs, and CTLs in that one physical store.

The high word of <i>dwFlags</i> indicates the system store location, usually set to CERT_SYSTEM_STORE_CURRENT_USER. For more information, see <i>dwFlags</i> later in this topic. Some system store locations can be open remotely; for more information, see <a href="/windows/desktop/SecCrypto/system-store-locations">System Store Locations</a>.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a null-terminated ANSI string that contains a system store name, such as "My" or "Root".

</td>
</tr>
<tr>
<td width="40%"><a id="_CERT_STORE_PROV_SYSTEM_REGISTRY__W_"></a><a id="_cert_store_prov_system_registry__w_"></a><dl>
<dt><b> CERT_STORE_PROV_SYSTEM_REGISTRY(_W)</b></dt>
<dt><b>sz_CERT_STORE_PROV_SYSTEM_REGISTRY(_W)</b></dt>
</dl>
</td>
<td width="60%">
Same as <b>CERT_STORE_PROV_SYSTEM_REGISTRY_A</b>.

<b><i>pvPara</i> value:  </b>The <i>pvPara</i> parameter points to a null-terminated Unicode string that contains a system store name, such as "My" or "Root".

</td>
</tr>
</table>

### -param dwEncodingType [in]

Specifies the <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a> and <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a>. Encoding is used only when the <i>dwSaveAs</i> parameter of  the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsavestore">CertSaveStore</a> function contains <b>CERT_STORE_SAVE_AS_PKCS7</b>. Otherwise, the <i>dwMsgAndCertEncodingType</i> parameter is not used.

This parameter is only applicable  when the <b>CERT_STORE_PROV_MSG</b>, <b>CERT_STORE_PROV_PKCS7</b>, or <b>CERT_STORE_PROV_FILENAME</b> provider type is specified in the <i>lpszStoreProvider</i> parameter. For all other provider types, this parameter is unused and should be set to zero.


This parameter can be a combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PKCS_7_ASN_ENCODING"></a><a id="pkcs_7_asn_encoding"></a><dl>
<dt><b>PKCS_7_ASN_ENCODING</b></dt>
<dt>65536 (0x10000)</dt>
</dl>
</td>
<td width="60%">
Specifies PKCS #7 message encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies X.509 certificate encoding.

</td>
</tr>
</table>

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to a cryptographic provider. Passing <b>NULL</b> for this parameter causes an appropriate, default provider to be used. Using the default provider is recommended. The default or specified cryptographic provider is used for all store functions that verify the signature of a subject certificate or CRL.This parameter's data type is <b>HCRYPTPROV</b>.

### -param dwFlags [in]

These values consist of high-word and low-word values combined by using a bitwise-<b>OR</b> operation.


The low-word portion of <i>dwFlags</i> controls a variety of general characteristics of the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> opened. This portion can be used with all store provider types. The low-word portion of <i>dwFlags</i> can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_BACKUP_RESTORE_FLAG"></a><a id="cert_store_backup_restore_flag"></a><dl>
<dt><b>CERT_STORE_BACKUP_RESTORE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Use the thread's SE_BACKUP_NAME and SE_RESTORE_NAME <a href="/windows/desktop/SecGloss/p-gly">privileges</a> to open registry or file-based system stores. If the thread does not have these privileges, this function must fail with an access denied error.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CREATE_NEW_FLAG"></a><a id="cert_store_create_new_flag"></a><dl>
<dt><b>CERT_STORE_CREATE_NEW_FLAG</b></dt>
</dl>
</td>
<td width="60%">
A new store is created if one did not exist. The function fails if the store already exists.

If neither <b>CERT_STORE_OPEN_EXISTING_FLAG</b> nor <b>CERT_STORE_CREATE_NEW_FLAG</b> is set, a store is opened if it exists or is created and opened if it did not already exist.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_DEFER_CLOSE_UNTIL_LAST_FREE_FLAG"></a><a id="cert_store_defer_close_until_last_free_flag"></a><dl>
<dt><b>CERT_STORE_DEFER_CLOSE_UNTIL_LAST_FREE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Defer closing of the store's provider until all certificates, CRLs, or CTLs obtained from the store are no longer in use. The store is actually closed when the last certificate, CRL, or CTL obtained from the store is freed. Any changes made to properties of these certificates, CRLs, and CTLs, even after the call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>, are persisted.

If this flag is not set and certificates, CRLs, or CTLs obtained from the store are still in use, any changes to the properties of those certificates, CRLs, and CTLs will not be persisted.

If this function is called with <b>CERT_CLOSE_STORE_FORCE_FLAG</b>, <b>CERT_STORE_DEFER_CLOSE_UNTIL_LAST_FREE_FLAG</b> is ignored.

When this flag is set and a non-<b>NULL</b> <i>hCryptProv</i> parameter value is passed, that provider will continue to be used even after the call to 
this function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_DELETE_FLAG"></a><a id="cert_store_delete_flag"></a><dl>
<dt><b>CERT_STORE_DELETE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The store is deleted instead of being opened. This function returns <b>NULL</b> for both success and failure of the deletion. To determine the success of the deletion, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns zero if the store was deleted and a nonzero value if it was not deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ENUM_ARCHIVED_FLAG"></a><a id="cert_store_enum_archived_flag"></a><dl>
<dt><b>CERT_STORE_ENUM_ARCHIVED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Normally, an enumeration of all certificates in the store will ignore any certificate with the <b>CERT_ARCHIVED_PROP_ID</b> property set. If this flag is set, an enumeration of the certificates in the store will contain all of the certificates in the store, including those that have the <b>CERT_ARCHIVED_PROP_ID</b> property.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_MAXIMUM_ALLOWED_FLAG"></a><a id="cert_store_maximum_allowed_flag"></a><dl>
<dt><b>CERT_STORE_MAXIMUM_ALLOWED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Open the store with the maximum set of allowed permissions. If this flag is specified, registry stores are first opened with write access and if that fails, they are reopened with read-only access.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_NO_CRYPT_RELEASE_FLAG"></a><a id="cert_store_no_crypt_release_flag"></a><dl>
<dt><b>CERT_STORE_NO_CRYPT_RELEASE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used when  the <i>hCryptProv</i> parameter is <b>NULL</b>. This flag is only valid when a non-<b>NULL</b> CSP handle is passed as the <i>hCryptProv</i> parameter. Setting this flag prevents the automatic release of a nondefault CSP when the certificate store is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_OPEN_EXISTING_FLAG"></a><a id="cert_store_open_existing_flag"></a><dl>
<dt><b>CERT_STORE_OPEN_EXISTING_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Only open an existing store. If the store does not exist, the function fails.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_READONLY_FLAG"></a><a id="cert_store_readonly_flag"></a><dl>
<dt><b>CERT_STORE_READONLY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Open the store in read-only mode. Any attempt to change the contents of the store will result in an error. When this flag is set and a registry based store provider is being used, the registry subkeys are opened by using <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeya">RegOpenKey</a> with <b>KEY_READ_ACCESS</b>. Otherwise, the registry subkeys are created by using <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeya">RegCreateKey</a> with <b>KEY_ALL_ACCESS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SET_LOCALIZED_NAME_FLAG"></a><a id="cert_store_set_localized_name_flag"></a><dl>
<dt><b>CERT_STORE_SET_LOCALIZED_NAME_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If this flag is supported, the provider sets the store's <b>CERT_STORE_LOCALIZED_NAME_PROP_ID</b> property. The localized name can be retrieved by calling 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetstoreproperty">CertGetStoreProperty</a> function with <i>dwPropID</i> set to 
<b>CERT_STORE_LOCALIZED_NAME_PROP_ID</b>. This flag is supported for providers of types <b>CERT_STORE_PROV_FILENAME</b>, <b>CERT_STORE_PROV_SYSTEM</b>, <b>CERT_STORE_PROV_SYSTEM_REGISTRY</b>, and <b>CERT_STORE_PROV_PHYSICAL_W</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SHARE_CONTEXT_FLAG"></a><a id="cert_store_share_context_flag"></a><dl>
<dt><b>CERT_STORE_SHARE_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
When opening a store multiple times, you can set  this flag  to ensure efficient memory usage by reusing the memory for the encoded parts of a certificate, CRL, or CTL context across the opened instances of the stores.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_UPDATE_KEYID_FLAG"></a><a id="cert_store_update_keyid_flag"></a><dl>
<dt><b>CERT_STORE_UPDATE_KEYID_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Lists of key identifiers exist within CurrentUser and LocalMachine. These key identifiers have properties much like the properties of certificates. If the <b>CERT_STORE_UPDATE_KEYID_FLAG</b> is set, then for every key identifier in the store's location that has a <b>CERT_KEY_PROV_INFO_PROP_ID</b> property, that property is automatically updated from the key identifier property <b>CERT_KEY_PROV_INFO_PROP_ID</b> or the <b>CERT_KEY_IDENTIFIER_PROP_ID</b> of the certificate related to that key identifier.

</td>
</tr>
</table>
 


The <b>CERT_STORE_PROV_SYSTEM</b>, 
<b>CERT_STORE_PROV_SYSTEM_REGISTRY</b>, and 
<b>CERT_STORE_PROV_PHYSICAL</b> provider types use the following high words of <i>dwFlags</i> to specify system store registry locations:



<a id="CERT_SYSTEM_STORE_CURRENT_SERVICE"></a>
<a id="cert_system_store_current_service"></a>


#### CERT_SYSTEM_STORE_CURRENT_SERVICE

<a id="CERT_SYSTEM_STORE_CURRENT_USER"></a>
<a id="cert_system_store_current_user"></a>


#### CERT_SYSTEM_STORE_CURRENT_USER

<a id="CERT_SYSTEM_STORE_CURRENT_USER_GROUP_POLICY"></a>
<a id="cert_system_store_current_user_group_policy"></a>


#### CERT_SYSTEM_STORE_CURRENT_USER_GROUP_POLICY

<a id="CERT_SYSTEM_STORE_LOCAL_MACHINE"></a>
<a id="cert_system_store_local_machine"></a>


#### CERT_SYSTEM_STORE_LOCAL_MACHINE

<a id="CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE"></a>
<a id="cert_system_store_local_machine_enterprise"></a>


#### CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE

<a id="CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY"></a>
<a id="cert_system_store_local_machine_group_policy"></a>


#### CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY

<a id="CERT_SYSTEM_STORE_SERVICES"></a>
<a id="cert_system_store_services"></a>


#### CERT_SYSTEM_STORE_SERVICES

<a id="CERT_SYSTEM_STORE_USERS"></a>
<a id="cert_system_store_users"></a>


#### CERT_SYSTEM_STORE_USERS


By default, a system store location is opened relative to the <b>HKEY_CURRENT_USER</b>, <b>HKEY_LOCAL_MACHINE</b>, or <b>HKEY_USERS</b> predefined registry key. For more information, see 
<a href="/windows/desktop/SecCrypto/system-store-locations">System Store Locations</a>.

The following high-word flags override this default behavior.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_RELOCATE_FLAG"></a><a id="cert_system_store_relocate_flag"></a><dl>
<dt><b>CERT_SYSTEM_STORE_RELOCATE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
When set, <i>pvPara</i> must contain a pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure rather than a string. The structure indicates both the name of the store and its location in the registry.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_UNPROTECTED_FLAG"></a><a id="cert_system_store_unprotected_flag"></a><dl>
<dt><b>CERT_SYSTEM_STORE_UNPROTECTED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
By default, when the CurrentUser "Root" store is opened, any SystemRegistry roots not on the protected root list are deleted from the cache before this function returns. When this flag is set, this default is overridden and all of the roots in the SystemRegistry are returned and no check of the protected root list is made.

</td>
</tr>
</table>
 


The <b>CERT_STORE_PROV_REGISTRY</b> provider uses the following high-word flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_REGISTRY_STORE_REMOTE_FLAG"></a><a id="cert_registry_store_remote_flag"></a><dl>
<dt><b>CERT_REGISTRY_STORE_REMOTE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
<i>pvPara</i> contains a handle to a registry key on a remote computer. To access a registry key on a remote computer, security permissions on the remote computer must be set to allow access. For more information, see  Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_REGISTRY_STORE_SERIALIZED_FLAG"></a><a id="cert_registry_store_serialized_flag"></a><dl>
<dt><b>CERT_REGISTRY_STORE_SERIALIZED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The <b>CERT_STORE_PROV_REG</b> provider saves certificates, CRLs, and CTLs in a single serialized store subkey instead of performing the default save operation. The default is that each certificate, CRL, or CTL is saved as a separate registry subkey under the appropriate subkey.

This flag is mainly used for stores downloaded from the group policy template (GPT), such as the CurrentUserGroupPolicy and LocalMachineGroupPolicy stores.

When <b>CERT_REGISTRY_STORE_SERIALIZED_FLAG</b> is set, store additions, deletions, or property changes are not persisted until there is a call to either 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a> using <b>CERT_STORE_CTRL_COMMIT</b>.

</td>
</tr>
</table>
 


The <b>CERT_STORE_PROV_FILE</b> and <b>CERT_STORE_PROV_FILENAME</b> provider types use the following high-word flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_FILE_STORE_COMMIT_ENABLE"></a><a id="cert_file_store_commit_enable"></a><dl>
<dt><b>CERT_FILE_STORE_COMMIT_ENABLE</b></dt>
</dl>
</td>
<td width="60%">
Setting this flag commits any additions to the store or any changes made to properties of contexts in the store to the file store either when 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> is called or when 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a> is called with <b>CERT_STORE_CONTROL_COMMIT</b>.

<b>CertOpenStore</b> fails with <b>E_INVALIDARG</b> if both <b>CERT_FILE_STORE_COMMIT_ENABLE</b> and <b>CERT_STORE_READONLY_FLAG</b> are set in <i>dwFlags</i>.

</td>
</tr>
</table>
 


The <b>CERT_STORE_PROV_LDAP</b> provider type uses the following high-word flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_LDAP_STORE_AREC_EXCLUSIVE_FLAG"></a><a id="cert_ldap_store_arec_exclusive_flag"></a><dl>
<dt><b>CERT_LDAP_STORE_AREC_EXCLUSIVE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Performs an A-Record-only DNS lookup on the URL named in the <i>pvPara</i> parameter. This prevents false DNS queries from being generated when resolving URL host names. Use this flag when passing a host name as opposed to a domain name for the <i>pvPara</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LDAP_STORE_OPENED_FLAG"></a><a id="cert_ldap_store_opened_flag"></a><dl>
<dt><b>CERT_LDAP_STORE_OPENED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Use this flag to use an existing LDAP session. When this flag is specified, the <i>pvPara</i> parameter is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_ldap_store_opened_para">CERT_LDAP_STORE_OPENED_PARA</a> structure that contains information about the LDAP session to use.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LDAP_STORE_SIGN_FLAG"></a><a id="cert_ldap_store_sign_flag"></a><dl>
<dt><b>CERT_LDAP_STORE_SIGN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
To provide integrity required by some applications, digitally sign all LDAP traffic to and from an LDAP server by using the Kerberos authentication protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LDAP_STORE_UNBIND_FLAG"></a><a id="cert_ldap_store_unbind_flag"></a><dl>
<dt><b>CERT_LDAP_STORE_UNBIND_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Use this flag with the <b>CERT_LDAP_STORE_OPENED_FLAG</b> flag to cause the LDAP session to be unbound when the store is closed. The system will unbind the LDAP session by using the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> function when the store is closed.

</td>
</tr>
</table>

### -param pvPara [in]

A 32-bit value that can contain additional information for this function. The contents of this parameter depends on the value of the <i>lpszStoreProvider</i> and other parameters.

## -returns

If the function succeeds, the function returns a handle to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. When you have finished using the store, release the handle by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

If the function fails, it returns <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>, <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>, or registry errors might be propagated and their error codes returned. <b>CertOpenStore</b> has a single error code of its own, the ERROR_FILE_NOT_FOUND code, which indicates that the function was unable to find the provider specified by the <i>lpszStoreProvider</i> parameter.</div>
<div> </div>

## -remarks

A system store is a collection that consists of one or more physical sibling stores. For each system store, there are predefined physical sibling stores. After opening a system store such as "My" at CERT_SYSTEM_STORE_CURRENT_USER, <b>CertOpenStore</b> is called to open all of the physical stores in the system store collection. Each of these physical stores is added to the system store collection by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a> function. All certificates, CRLs, and CTLs in those physical stores are available through the logical system store collection.

<div class="alert"><b>Note</b>  The order of the certificate context may not be preserved within the store. 
To access a specific certificate you must iterate across the certificates in the store.</div>
<div> </div>

The following system store locations can be opened remotely:

<ul>
<li>CERT_SYSTEM_STORE_LOCAL_MACHINE</li>
<li>CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY</li>
<li>CERT_SYSTEM_STORE_SERVICES</li>
<li>CERT_SYSTEM_STORE_USERS</li>
</ul>



System store locations are opened remotely by prefixing the store name in the string passed to <i>pvPara</i> with the computer name. Examples of remote system store names are:

<ul>
<li><i>ComputerName</i>&#92;<i>CA</i></li>
<li>&#92;&#92;<i>ComputerName</i>&#92;<i>CA</i></li>
<li><i>ComputerName</i>&#92;<i>ServiceName</i>&#92;<i>Trust</i></li>
<li>&#92;&#92;<i>ComputerName</i>&#92;<i>ServiceName</i>&#92;<i>Trust</i></li>
</ul>


For more information about system stores, see 
<a href="/windows/desktop/SecCrypto/system-store-locations">System Store Locations</a>.

For more information about the stores that are automatically migrated, see <a href="/windows/desktop/SecCrypto/certificate-store-migration">Certificate Store Migration</a>.


#### Examples

The following example shows opening several certificate stores of different store provider types.  The example uses the <b>CreateMyDACL</b> function, defined in the <a href="/windows/desktop/SecBP/creating-a-dacl">Creating a DACL</a> topic, to ensure  the open file is created with a proper DACL. For more examples of opening other store provider types, see 
<a href="/windows/desktop/SecCrypto/example-c-code-for-opening-certificate-stores">Example C Code for Opening Certificate Stores</a>.


```cpp
//-------------------------------------------------------------------
// Open a system store, in this case, the My store.

HCERTSTORE hSysStore = NULL;
if(hSysStore = CertOpenStore(
   CERT_STORE_PROV_SYSTEM,          // The store provider type
   0,                               // The encoding type is
                                    // not needed
   NULL,                            // Use the default HCRYPTPROV
   CERT_SYSTEM_STORE_CURRENT_USER,  // Set the store location in a
                                    // registry location
   L"MY"                            // The store name as a Unicode 
                                    // string
   ))
{
    printf("The system store was created successfully.\n");
}
else
{
    printf("An error occurred during creation "
        "of the system store!\n");
    exit(1);
}

// Other common system stores include "Root", "Trust", and "Ca".


//-------------------------------------------------------------------
// Open a memory store. 

HCERTSTORE hMemStore = NULL;
if(hMemStore = CertOpenStore(
   CERT_STORE_PROV_MEMORY,   // The memory provider type
   0,                        // The encoding type is not needed
   NULL,                     // Use the default HCRYPTPROV
   0,                        // Accept the default dwFlags
   NULL                      // pvPara is not used
   ))
{
    printf("The memory store was created successfully.\n");
}
else
{
    printf("An error occurred during creation "
        "of the memory store!\n");
    exit(1);
}

//-------------------------------------------------------------------
// Open a read-only store from disk.

HANDLE       hFile = NULL;
HCERTSTORE   hFileStore = NULL;
LPCSTR       pszFileName = "TestStor2.sto";
SECURITY_ATTRIBUTES  sa;        // For DACL

// Create a DACL to use when opening the file.
sa.nLength = sizeof(SECURITY_ATTRIBUTES);
sa.bInheritHandle = FALSE;  

// Call function to set the DACL. The DACL is set in the 
// SECURITY_ATTRIBUTES lpSecurityDescriptor member.
if (!CreateMyDACL(&sa))
{
     // Error encountered; generate message and exit.
     printf("Failed CreateMyDACL.\n");
        exit(1);
}

// Obtain the file handle of an existing file.
if (hFile = CreateFile(
     pszFileName,                  // The file name
     GENERIC_READ|GENERIC_WRITE,   // Access mode: Read from and
                                   // write to this file
     0,                            // Share mode
     &sa,                          // Uses the DACL created 
                                   // previously 
     OPEN_ALWAYS,                  // How to create
     FILE_ATTRIBUTE_NORMAL,        // File attributes
     NULL))                        // Template
{
    printf("The file was opened successfully.\n");
}
else
{
    printf("An error occurred during opening of the file!\n");
    exit(1);
}

//-------------------------------------------------------------------
//  This file can contain data before the store itself.
//  At this point, read and use data in the open file that precedes
//  the serialized certificate store data. 
//  To open the certificate store, the file pointer must
//  be placed at the beginning of the certificate store data.

//-------------------------------------------------------------------
//  Open the store.

if(hFileStore = CertOpenStore(
    CERT_STORE_PROV_FILE,     // Load certificates from a file
    0,                        // Encoding type not used
    NULL,                     // Use the default HCRYPTPROV
    CERT_STORE_READONLY_FLAG, // Read-only store
    hFile                     // The handle for the open file 
                              // that is the source of the 
                              // certificates
    ))
{
    printf("The file store was created successfully.\n");
}
else
{
    printf("An error occurred during creation of the file store!\n");
    exit(1);
}

//-------------------------------------------------------------------
// After processing, close the certificate stores and the file.

if(CertCloseStore(
        hSysStore, 
        CERT_CLOSE_STORE_CHECK_FLAG))
{
    printf("The system store was closed successfully.\n");
}
else
{
    printf("An error occurred during closing of the "
        "system store.\n");
}

if(CertCloseStore(
        hMemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG))
{
    printf("The memory store was closed successfully.\n");
}
else
{
    printf("An error occurred during closing of the "
        "memory store.\n");
}

if(CertCloseStore(
        hFileStore, 
        CERT_CLOSE_STORE_CHECK_FLAG))
{
    printf("The file store was closed successfully.\n");
}
else
{
    printf("An error occurred during closing of the file store.\n");
}

if(CloseHandle(hFile))
{
    printf("The file was closed successfully.\n");
}
else
{
    printf("An error occurred during closing of the file.\n");
}

```

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsavestore">CertSaveStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>