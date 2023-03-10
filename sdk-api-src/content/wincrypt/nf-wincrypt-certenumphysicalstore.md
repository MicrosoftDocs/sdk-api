---
UID: NF:wincrypt.CertEnumPhysicalStore
title: CertEnumPhysicalStore function (wincrypt.h)
description: The CertEnumPhysicalStore function retrieves the physical stores on a computer. The function calls the provided callback function for each physical store found.
helpviewer_keywords: ["CertEnumPhysicalStore","CertEnumPhysicalStore function [Security]","_crypto2_certenumphysicalstore","security.certenumphysicalstore","wincrypt/CertEnumPhysicalStore"]
old-location: security\certenumphysicalstore.htm
tech.root: security
ms.assetid: 5804d565-5129-4e6d-8b3d-9bd938807740
ms.date: 12/05/2018
ms.keywords: CertEnumPhysicalStore, CertEnumPhysicalStore function [Security], _crypto2_certenumphysicalstore, security.certenumphysicalstore, wincrypt/CertEnumPhysicalStore
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
 - CertEnumPhysicalStore
 - wincrypt/CertEnumPhysicalStore
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
 - CertEnumPhysicalStore
---

# CertEnumPhysicalStore function


## -description

The <b>CertEnumPhysicalStore</b> function retrieves the physical stores on a computer. The function calls the provided callback function for each physical store found.

## -parameters

### -param pvSystemStore [in]

If CERT_SYSTEM_STORE_RELOCATE_FLAG is set in <i>dwFlags</i>, <i>pvSystemStore</i> points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure that indicates both the name and the location of the system store to be enumerated. Otherwise, <i>pvSystemStore</i> is a pointer to a Unicode string that names the system store whose physical stores are to be enumerated. For information about prefixing a ServiceName or ComputerName to the system store name, see 
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
In addition, CERT_SYSTEM_STORE_RELOCATE_FLAG or CERT_PHYSICAL_STORE_PREDEFINED_ENUM_FLAG can be combined using a bitwise-<b>OR</b> operation with any of the high-word location flags.

### -param pvArg [in]

A pointer to a <b>void</b> that allows the application to declare, define, and initialize a structure to hold any information to be passed to the callback enumeration function.

### -param pfnEnum [in]

A pointer to the callback function used to show the details for each physical store. This callback function determines the content and format for the presentation of information on each physical store. The application must provide the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_enum_physical_store">CertEnumPhysicalStoreCallback</a> callback function.

## -returns

If the function succeeds and another physical store was found, the return value is <b>TRUE</b>.

If the system store location only supports system stores and does not support physical stores, the function returns <b>FALSE</b> and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the ERROR_NOT_SUPPORTED code.

If the function fails and another physical store was not found, the return value is <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To use <b>CertEnumPhysicalStore</b>, an application must declare and define the <b>ENUM_ARG</b> structure and an enumeration callback function.


#### Examples

See 
<a href="/windows/desktop/SecCrypto/example-c-program-listing-system-and-physical-stores">Example C Program: Listing System and Physical Stores</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstore">CertEnumSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregistersystemstore">CertUnregisterSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>