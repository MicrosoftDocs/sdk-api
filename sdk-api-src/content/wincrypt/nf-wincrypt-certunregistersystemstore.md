---
UID: NF:wincrypt.CertUnregisterSystemStore
title: CertUnregisterSystemStore function (wincrypt.h)
description: The CertUnregisterSystemStore function unregisters a specified system store.
helpviewer_keywords: ["CERT_STORE_DELETE_FLAG","CERT_SYSTEM_STORE_RELOCATE_FLAG","CertUnregisterSystemStore","CertUnregisterSystemStore function [Security]","_crypto2_certunregistersystemstore","security.certunregistersystemstore","wincrypt/CertUnregisterSystemStore"]
old-location: security\certunregistersystemstore.htm
tech.root: security
ms.assetid: 958e4185-4c37-450c-abfc-91b95593227e
ms.date: 12/05/2018
ms.keywords: CERT_STORE_DELETE_FLAG, CERT_SYSTEM_STORE_RELOCATE_FLAG, CertUnregisterSystemStore, CertUnregisterSystemStore function [Security], _crypto2_certunregistersystemstore, security.certunregistersystemstore, wincrypt/CertUnregisterSystemStore
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
 - CertUnregisterSystemStore
 - wincrypt/CertUnregisterSystemStore
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
 - CertUnregisterSystemStore
---

# CertUnregisterSystemStore function


## -description

The <b>CertUnregisterSystemStore</b> function unregisters a specified system store.

## -parameters

### -param pvSystemStore [in]

Identifies the system store to be unregistered. It points either to a null-terminated Unicode string or to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure. For information about using the structure and on appending a ServiceName or ComputerName to the end of the system store name string, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>.

### -param dwFlags [in]

The high word of the <i>dwFlags</i> parameter specifies the location of the system store. For information about defined high-word flags and on appending ServiceName, UserNames, and ComputerNames to the end of the system store name, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>. 




The following low-word values are also defined and can be combined with high-word values using a bitwise-<b>OR</b> operation.

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
The system store is deleted after it has been unregistered.

</td>
</tr>
</table>

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



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>