---
UID: NC:wincrypt.PFN_CERT_ENUM_PHYSICAL_STORE
title: PFN_CERT_ENUM_PHYSICAL_STORE (wincrypt.h)
description: The CertEnumPhysicalStoreCallback callback function formats and presents information on each physical store found by a call to CertEnumPhysicalStore.
helpviewer_keywords: ["CertEnumPhysicalStoreCallback","PFN_CERT_ENUM_PHYSICAL_STORE","PFN_CERT_ENUM_PHYSICAL_STORE callback","PFN_CERT_ENUM_PHYSICAL_STORE callback function [Security]","security.certenumphysicalstorecallback","wincrypt/PFN_CERT_ENUM_PHYSICAL_STORE"]
old-location: security\certenumphysicalstorecallback.htm
tech.root: security
ms.assetid: 0651730a-39f2-4598-a81c-d05e6d282e6c
ms.date: 12/05/2018
ms.keywords: CertEnumPhysicalStoreCallback, PFN_CERT_ENUM_PHYSICAL_STORE, PFN_CERT_ENUM_PHYSICAL_STORE callback, PFN_CERT_ENUM_PHYSICAL_STORE callback function [Security], security.certenumphysicalstorecallback, wincrypt/PFN_CERT_ENUM_PHYSICAL_STORE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CERT_ENUM_PHYSICAL_STORE
 - wincrypt/PFN_CERT_ENUM_PHYSICAL_STORE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_ENUM_PHYSICAL_STORE
---

# PFN_CERT_ENUM_PHYSICAL_STORE callback function


## -description

The <b>CertEnumPhysicalStoreCallback</b> 
    callback function formats and presents information on each physical store found by a call to 
    <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumphysicalstore">CertEnumPhysicalStore</a>.

## -parameters

### -param pvSystemStore [in]

If CERT_SYSTEM_STORE_RELOCATE_FLAG is set in <i>dwFlags</i>, <i>pvSystemStore</i> points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure that indicates both the name and the location of the system store to be enumerated. Otherwise, <i>pvSystemStore</i> is a pointer to a Unicode string that names the system store whose physical stores are to be enumerated. For information about prefixing the name of a service or computer to the system store name, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>.

### -param dwFlags [in]

Specifies the location of the system store. The following flag values are defined:

<ul>
<li>CERT_SYSTEM_STORE_CURRENT_USER</li>
<li>CERT_SYSTEM_STORE_CURRENT_SERVICE</li>
<li>CERT_SYSTEM_STORE_LOCAL_MACHINE</li>
<li>CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY</li>
<li>CERT_SYSTEM_STORE_CURRENT_USER_GROUP_POLICY</li>
<li>CERT_SYSTEM_STORE_SERVICES</li>
<li>CERT_SYSTEM_STORE_USERS</li>
<li>CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE</li>
</ul>
In addition, CERT_SYSTEM_STORE_RELOCATE_FLAG or CERT_PHYSICAL_STORE_PREDEFINED_ENUM_FLAG can be combined using a bitwise-<b>OR</b> operation with any of the high-word location flags. The CERT_PHYSICAL_STORE_PREDEFINED_ENUM_FLAG constant is set if the physical store is predefined rather than registered.

### -param pwszStoreName [in]

Name of the physical store.

### -param pStoreInfo [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_physical_store_info">CERT_PHYSICAL_STORE_INFO</a> structure containing information about the store.

### -param pvReserved [in]

Reserved for future use.

### -param pvArg [in]

A pointer to information passed to the callback function in the <i>pvArg</i> passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumphysicalstore">CertEnumPhysicalStore</a>.

## -returns

Returns <b>TRUE</b> if the function succeeds, <b>FALSE</b> if it fails.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstore">CertEnumSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregistersystemstore">CertUnregisterSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>
