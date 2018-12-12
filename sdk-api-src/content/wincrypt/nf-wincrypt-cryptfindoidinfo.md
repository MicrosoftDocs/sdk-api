---
UID: NF:wincrypt.CryptFindOIDInfo
title: CryptFindOIDInfo function
author: windows-sdk-content
description: Retrieves the first predefined or registered CRYPT_OID_INFO structure that matches a specified key type and key. The search can be limited to object identifiers (OIDs) within a specified OID group.
old-location: security\cryptfindoidinfo.htm
tech.root: seccrypto
ms.assetid: 87acf207-d109-4173-9530-8cbbebb473b2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CRYPT_OID_DISABLE_SEARCH_DS_FLAG, CRYPT_OID_INFO_ALGID_KEY, CRYPT_OID_INFO_CNG_ALGID_KEY, CRYPT_OID_INFO_CNG_SIGN_KEY, CRYPT_OID_INFO_NAME_KEY, CRYPT_OID_INFO_OID_KEY, CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, CRYPT_OID_INFO_SIGN_KEY, CryptFindOIDInfo, CryptFindOIDInfo function [Security], _crypto2_cryptfindoidinfo, security.cryptfindoidinfo, wincrypt/CryptFindOIDInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptFindOIDInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptFindOIDInfo function


## -description


The <b>CryptFindOIDInfo</b> function retrieves the first predefined or registered 
<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structure that matches a specified key type and key. The search can be limited to <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) within a specified OID group.

Use 
<a href="https://msdn.microsoft.com/6af23bb4-3a27-425a-90bb-9a69ea081b25">CryptEnumOIDInfo</a> to list all or selected subsets of <a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structures. New <b>CRYPT_OID_INFO</b> structures can be registered by using 
<a href="https://msdn.microsoft.com/7a5b4800-3182-4cd4-b17a-c6d4e11f7047">CryptRegisterOIDInfo</a>. User-registered OIDs can be removed from the list of registered OIDs by using 
<a href="https://msdn.microsoft.com/1217397b-2af9-4f58-8616-5a18ee2f4b8c">CryptUnregisterOIDInfo</a>.

New OIDs can be placed in the list of registered OIDs either before or after the predefined entries. Because <b>CryptFindOIDInfo</b> returns the first key on the list that matches the search criteria, a newly registered OID placed before a predefined OID entry with the same key overrides a predefined entry.


## -parameters




### -param dwKeyType [in]

Specifies the key type to use when finding OID information. 


This parameter can be one of the following key types.



#### CRYPT_OID_INFO_OID_KEY

<i>pvKey</i> is the address of a null-terminated ANSI string that contains the OID string to find.



#### CRYPT_OID_INFO_NAME_KEY

<i>pvKey</i> is the address of a null-terminated Unicode string that contains the name to find.



#### CRYPT_OID_INFO_ALGID_KEY

<i>pvKey</i> is the address of an 
<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>variable. The following <b>ALG_ID</b>s are supported:

Hash Algorithms:

Symmetric Encryption Algorithms:

Public Key Algorithms:

Algorithms that are not listed are supported by using <a href="https://msdn.microsoft.com/eaad88a1-4e1d-4246-9560-8eef60f8b70f">Cryptography API: Next Generation</a> (CNG) only; instead, use <b>CRYPT_OID_INFO_CNG_ALGID_KEY</b>.



#### CRYPT_OID_INFO_SIGN_KEY

<i>pvKey</i> is the address of an array of two <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>s where the first element contains the hash algorithm identifier and the second element contains the public key algorithm identifier.

The following <b>ALG_ID</b> combinations are supported.

<table>
<tr>
<th>Signature algorithm identifier</th>
<th>Hash algorithm identifier</th>
</tr>
<tr>
<td>
CALG_RSA_SIGN

</td>
<td>

<dl>
<dd>CALG_SHA1</dd>
<dd>CALG_MD5</dd>
<dd>CALG_MD4</dd>
<dd>CALG_MD2</dd>
</dl>


</td>
</tr>
<tr>
<td>
CALG_DSS_SIGN

</td>
<td>

<dl>
<dd>CALG_SHA1</dd>
</dl>


</td>
</tr>
<tr>
<td>
CALG_NO_SIGN

</td>
<td>

<dl>
<dd>CALG_SHA1</dd>
<dd>CALG_NO_SIGN</dd>
</dl>


</td>
</tr>
</table>
 

Algorithms that are not listed are supported through CNG only; instead, use <b>CRYPT_OID_INFO_CNG_SIGN_KEY</b>.



#### CRYPT_OID_INFO_CNG_ALGID_KEY


<i>pvKey</i> is the address of a null-terminated Unicode string that contains the CNG algorithm identifier to find. This can be one of the predefined <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> or another registered algorithm identifier.

<b>
                    Windows Server 2003 R2
                    Windows Server 2003
                  :  </b>This key type is not supported.



#### CRYPT_OID_INFO_CNG_SIGN_KEY


<i>pvKey</i> is the address of an array of two null-terminated Unicode string pointers where the first string contains the hash CNG algorithm identifier and the second string contains the public key CNG algorithm identifier. These can be from the predefined <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> or another registered algorithm identifier.

<b>
                    Windows Server 2003 R2
                    Windows Server 2003
                  :  </b>This key type is not supported.


Optionally, the following key types can be specified in the <i>dwKeyType</i> parameter by using the logical <b>OR</b> operator (|).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG"></a><a id="crypt_oid_info_pubkey_sign_key_flag"></a><dl>
<dt><b>CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Skips public keys in the CRYPT_PUBKEY_ALG_OID_GROUP_ID group that are explicitly flagged with the CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG"></a><a id="crypt_oid_info_pubkey_encrypt_key_flag"></a><dl>
<dt><b>CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Skips public keys in the CRYPT_PUBKEY_ALG_OID_GROUP_ID group that are explicitly flagged with the CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG flag.

</td>
</tr>
</table>
 


### -param pvKey [in]

The address of a buffer that contains additional search information. This parameter depends on the value of the <i>dwKeyType</i> parameter. For more information, see the table under <i>dwKeyType</i>.


### -param dwGroupId [in]

The group identifier to use when finding OID information. Setting this parameter to zero searches all groups according to the <i>dwKeyType</i> parameter. Otherwise, only the indicated <i>dwGroupId</i> is searched.

For information about code that lists the OID information by group identifier, see 
<a href="https://msdn.microsoft.com/6af23bb4-3a27-425a-90bb-9a69ea081b25">CryptEnumOIDInfo</a>.


Optionally, the following flag can be specified in the <i>dwGroupId</i> parameter by using the logical <b>OR</b> operator (|).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_DISABLE_SEARCH_DS_FLAG"></a><a id="crypt_oid_disable_search_ds_flag"></a><dl>
<dt><b>CRYPT_OID_DISABLE_SEARCH_DS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Disables searching the directory server.

</td>
</tr>
</table>
 

The bit length shifted left 16 bits can be specified in the <i>dwGroupId</i> parameter by using the logical <b>OR</b> operator (|). For more information, see Remarks.


## -returns



Returns a pointer to a constant structure of type <a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a>. The returned pointer must not be freed. When the specified key and group is not found, <b>NULL</b> is returned.




## -remarks



The <b>CryptFindOIDInfo</b> function performs a lookup in the active directory to retrieve the friendly names of OIDs under the following conditions:
<ul>
<li>The key type  in the <i>dwKeyType</i> parameter is set to <b>CRYPT_OID_INFO_OID_KEY</b> or <b>CRYPT_OID_INFO_NAME_KEY</b>.</li>
<li>No group identifier is specified in the  <i>dwGroupId</i> parameter or the GroupID refers to EKU OIDs, policy OIDs or template OIDs.</li>
</ul>Network retrieval of the friendly name can be suppressed by calling the function with the <b>CRYPT_OID_DISABLE_SEARCH_DS_FLAG</b> flag.

The bit length shifted left 16 bits can be specified in the <i>dwGroupId</i> parameter by using the logical <b>OR</b> operator (|). This is only applicable to the <b>CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b> group entries that have a bit length specified in the <b>ExtraInfo</b> member of the <a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structure. Currently, only the AES encryption algorithms have this. The constant <b>CRYPT_OID_INFO_OID_GROUP_BIT_LEN_SHIFT</b> can be used for doing the shift. For example, to find the OID information for <b>BCRYPT_AES_ALGORITHM</b> with bit length equal to 192, call <b>CryptFindOIDInfo</b> as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
DWORD dwBitLen = 192;

PCCRYPT_OID_INFO pOIDInfo = CryptFindOIDInfo(
     CRYPT_OID_INFO_CNG_ALGID_KEY,
     (void *) BCRYPT_AES_ALGORITHM,
     CRYPT_ENCRYPT_ALG_OID_GROUP_ID |
         (dwBitLen &lt;&lt; CRYPT_OID_INFO_OID_GROUP_BIT_LEN_SHIFT)
     );

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a>



<a href="https://msdn.microsoft.com/7a5b4800-3182-4cd4-b17a-c6d4e11f7047">CryptRegisterOIDInfo</a>



<a href="https://msdn.microsoft.com/1217397b-2af9-4f58-8616-5a18ee2f4b8c">CryptUnregisterOIDInfo</a>



<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

