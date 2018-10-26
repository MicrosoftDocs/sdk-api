---
UID: NF:wincrypt.CryptRegisterOIDInfo
title: CryptRegisterOIDInfo function
author: windows-sdk-content
description: The CryptRegisterOIDInfo function registers the OID information specified in the CRYPT_OID_INFO structure, persisting it to the registry.
old-location: security\cryptregisteroidinfo.htm
tech.root: seccrypto
ms.assetid: 7a5b4800-3182-4cd4-b17a-c6d4e11f7047
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CryptRegisterOIDInfo, CryptRegisterOIDInfo function [Security], _crypto2_cryptregisteroidinfo, security.cryptregisteroidinfo, wincrypt/CryptRegisterOIDInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptRegisterOIDInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptRegisterOIDInfo function


## -description


The <b>CryptRegisterOIDInfo</b> function registers the OID information specified in the 
<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structure, persisting it to the registry.

Crypt32.dll contains predefined information for the commonly known OIDs. This function allows applications to augment the predefined OID information. During 
<b>CryptRegisterOIDInfo</b>'s first call, the registered OID information is installed.

When expanding the tables using <b>CryptRegisterOIDInfo</b>, the new entries can be placed either before or after predefined entries, controlled by <i>dwFlags</i>. The placement of registered OID information affects the result of <a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a> because the tables are searched in order. First registered entries placed before the predefined entries are checked, then the predefined entries are checked, and finally, registered entries placed after the predefined entries are checked. The first match found is returned. A newly registered entry placed before the predefined entries can override one of the predefined entries.


## -parameters




### -param pInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structure with the OID information to register. Specify the group that the OID information is to be registered for by setting the <b>dwGroupId</b> member of the structure.

<div class="alert"><b>Note</b>  <p class="note">When registering OID information for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Suite B</a> algorithms implemented with <a href="https://msdn.microsoft.com/eaad88a1-4e1d-4246-9560-8eef60f8b70f">Cryptography API: Next Generation</a> (CNG), you must set the <b>Algid</b> member of the <a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structure to <b>CALG_OID_INFO_CNG_ONLY</b> (0xFFFFFFFF).

</div>
<div> </div>

### -param dwFlags [in]

By default, the registered OID information is installed after Crypt32.dll's OID entries. If CRYPT_INSTALL_OID_INFO_BEFORE_FLAG is set, new OID information is install before Crypt32.dll's entries.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).




## -remarks



When you have finished using the OID information, unregister it by calling the <a href="https://msdn.microsoft.com/1217397b-2af9-4f58-8616-5a18ee2f4b8c">CryptUnregisterOIDInfo</a>  function.




## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a>



<a href="https://msdn.microsoft.com/6af23bb4-3a27-425a-90bb-9a69ea081b25">CryptEnumOIDInfo</a>



<a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a>



<a href="https://msdn.microsoft.com/1217397b-2af9-4f58-8616-5a18ee2f4b8c">CryptUnregisterOIDInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">OID Support Functions</a>
 

 

