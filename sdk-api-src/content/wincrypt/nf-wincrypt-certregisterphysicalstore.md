---
UID: NF:wincrypt.CertRegisterPhysicalStore
title: CertRegisterPhysicalStore function (wincrypt.h)
description: Adds a physical store to a registry system store collection.
helpviewer_keywords: ["CERT_STORE_CREATE_NEW_FLAG","CERT_SYSTEM_STORE_RELOCATE_FLAG","CertRegisterPhysicalStore","CertRegisterPhysicalStore function [Security]","_crypto2_certregisterphysicalstore","security.certregisterphysicalstore","wincrypt/CertRegisterPhysicalStore"]
old-location: security\certregisterphysicalstore.htm
tech.root: security
ms.assetid: e301c76d-cacd-441a-b925-754b07e4bfa9
ms.date: 12/05/2018
ms.keywords: CERT_STORE_CREATE_NEW_FLAG, CERT_SYSTEM_STORE_RELOCATE_FLAG, CertRegisterPhysicalStore, CertRegisterPhysicalStore function [Security], _crypto2_certregisterphysicalstore, security.certregisterphysicalstore, wincrypt/CertRegisterPhysicalStore
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
 - CertRegisterPhysicalStore
 - wincrypt/CertRegisterPhysicalStore
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
 - CertRegisterPhysicalStore
---

# CertRegisterPhysicalStore function


## -description

The <b>CertRegisterPhysicalStore</b> function adds a physical store to a registry system store collection.

## -parameters

### -param pvSystemStore [in]

The system store collection to which the physical store is added. This parameter points either to a <b>null</b>-terminated Unicode string or to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure. For information about using the structure and on adding a ServiceName or ComputerName before the system store name string, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>.

### -param dwFlags [in]

The high word of the <i>dwFlags</i> parameter specifies the location of the system store. For information about defined high-word flags and appending ServiceName, UserNames, and ComputerNames to the end of the system store name, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>. 




The following low-word flags are also defined and can be combined with high-word flags using a bitwise-<b>OR</b> operation.

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
The system store is not in its default registry location and the <i>pvSystemStore</i> parameter must be a pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CREATE_NEW_FLAG"></a><a id="cert_store_create_new_flag"></a><dl>
<dt><b>CERT_STORE_CREATE_NEW_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The function fails if the physical store already exists in the store location.

</td>
</tr>
</table>

### -param pwszStoreName [in]

A pointer to a Unicode string that names the physical store to be added to the system store collection. To remove a physical store from the system store collection, call the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a> function.

### -param pStoreInfo [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_physical_store_info">CERT_PHYSICAL_STORE_INFO</a> structure that provides basic information about the physical store.

### -param pvReserved [in]

Reserved for future use and must be set to <b>NULL</b>.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_physical_store_info">CERT_PHYSICAL_STORE_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumphysicalstore">CertEnumPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstore">CertEnumSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>