---
UID: NF:wincrypt.CertEnumSystemStore
title: CertEnumSystemStore function (wincrypt.h)
description: The CertEnumSystemStore function retrieves the system stores available. The function calls the provided callback function for each system store found.
helpviewer_keywords: ["CertEnumSystemStore","CertEnumSystemStore function [Security]","_crypto2_certenumsystemstore","security.certenumsystemstore","wincrypt/CertEnumSystemStore"]
old-location: security\certenumsystemstore.htm
tech.root: security
ms.assetid: fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac
ms.date: 12/05/2018
ms.keywords: CertEnumSystemStore, CertEnumSystemStore function [Security], _crypto2_certenumsystemstore, security.certenumsystemstore, wincrypt/CertEnumSystemStore
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
 - CertEnumSystemStore
 - wincrypt/CertEnumSystemStore
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
 - CertEnumSystemStore
---

# CertEnumSystemStore function


## -description

The <b>CertEnumSystemStore</b> function retrieves the system stores available. The function calls the provided callback function for each system store found.

## -parameters

### -param dwFlags [in]

Specifies the location of the system store. This parameter can be one of the following flags: 




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
In addition, the CERT_SYSTEM_STORE_RELOCATE_FLAG can be combined, by using a bitwise-<b>OR</b> operation, with any of the high-word location flags.

### -param pvSystemStoreLocationPara [in, optional]

If CERT_SYSTEM_STORE_RELOCATE_FLAG is set in the <i>dwFlags</i> parameter, <i>pvSystemStoreLocationPara</i> points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure that indicates both the name and the location of the system store. Otherwise, <i>pvSystemStoreLocationPara</i> is a pointer to a Unicode string that names the system store. 




For CERT_SYSTEM_STORE_LOCAL_MACHINE or CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY, <i>pvSystemStoreLocationPara</i> can optionally be set to a Unicode computer name for enumerating local computer stores on a remote computer, for example "&#92;&#92;<i>computer_name</i>" or "<i>computer_name</i>". The leading backslashes (\\) are optional in the <i>computer_name</i>.

For CERT_SYSTEM_STORE_SERVICES or CERT_SYSTEM_STORE_USERS, if <i>pvSystemStoreLocationPara</i> is <b>NULL</b>, the function enumerates both the service/user names and the stores for each service/user name. Otherwise, <i>pvSystemStoreLocationPara</i> is a Unicode string that contains a remote computer name and, if available, a service/user name, for example, "<i>service_name</i>", "&#92;&#92;<i>computer_name</i>", or "<i>computer_name</i>\".

If only the <i>computer_name</i> is specified, it must have either the leading backslashes (\\) or a trailing backslash (\\). Otherwise, it is interpreted as the <i>service_name</i> or <i>user_name</i>.

### -param pvArg [in]

A pointer to a <b>void</b>  that allows the application to declare, define, and initialize a structure to hold any information to be passed to the callback enumeration function.

### -param pfnEnum [in]

A pointer to the callback function used to show the details for each system store. This callback function determines the content and format for the presentation of information on each system store. The application must provide the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_enum_system_store">CertEnumSystemStoreCallback</a> callback function.

## -returns

If the function succeeds, the function returns  <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>.

## -remarks

To use <b>CertEnumSystemStore</b>, the application must declare and define the <b>ENUM_ARG</b> structure and the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_enum_system_store">CertEnumSystemStoreCallback</a> callback function.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-listing-system-and-physical-stores">Example C Program: Listing System and Physical Stores</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_system_store_relocate_para">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumphysicalstore">CertEnumPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certunregistersystemstore">CertUnregisterSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>