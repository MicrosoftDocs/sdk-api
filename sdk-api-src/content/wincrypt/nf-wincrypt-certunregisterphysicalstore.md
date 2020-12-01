---
UID: NF:wincrypt.CertUnregisterPhysicalStore
title: CertUnregisterPhysicalStore function (wincrypt.h)
description: The CertUnregisterPhysicalStore function removes a physical store from a specified system store collection. CertUnregisterPhysicalStore can also be used to delete the physical store.
helpviewer_keywords: ["CERT_STORE_DELETE_FLAG","CERT_SYSTEM_STORE_RELOCATE_FLAG","CertUnregisterPhysicalStore","CertUnregisterPhysicalStore function [Security]","_crypto2_certunregisterphysicalstore","security.certunregisterphysicalstore","wincrypt/CertUnregisterPhysicalStore"]
old-location: security\certunregisterphysicalstore.htm
tech.root: security
ms.assetid: 06480a2f-5a94-4cf5-9774-ceb9499e1d44
ms.date: 12/05/2018
ms.keywords: CERT_STORE_DELETE_FLAG, CERT_SYSTEM_STORE_RELOCATE_FLAG, CertUnregisterPhysicalStore, CertUnregisterPhysicalStore function [Security], _crypto2_certunregisterphysicalstore, security.certunregisterphysicalstore, wincrypt/CertUnregisterPhysicalStore
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertUnregisterPhysicalStore
 - wincrypt/CertUnregisterPhysicalStore
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
 - CertUnregisterPhysicalStore
---

# CertUnregisterPhysicalStore function


## -description

The <b>CertUnregisterPhysicalStore</b> function removes a physical store from a specified system store collection. <b>CertUnregisterPhysicalStore</b> can also be used to delete the physical store.

## -parameters

### -param pvSystemStore [in]

A pointer to an identifier of the system store collection from which the physical store is to be removed. It is either to a null-terminated Unicode string or to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure. For information about using the structure and on appending a ServiceName or ComputerName to the end of the system store name string, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>.

### -param dwFlags [in]

The high word of the <i>dwFlags</i> parameter specifies the location of the system store. For information about defined high-word flags and on appending ServiceName, UserNames, and ComputerNames to the end of the system store name, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>. 



						
					


The following low-word values are also defined. They can be combined using bitwise-<b>OR</b> operations with high-word values.



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
The system store is not in its default registry location and <i>pvSystemStore</i> must be a pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_DELETE_FLAG"></a><a id="cert_store_delete_flag"></a><dl>
<dt><b>CERT_STORE_DELETE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The physical store is first removed from the system store collection and is then deleted.

</td>
</tr>
</table>

### -param pwszStoreName [in]

Null-terminated Unicode string that contains the name of the physical store.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumphysicalstore">CertEnumPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstore">CertEnumSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>