---
UID: NF:wincrypt.CertEnumSystemStoreLocation
title: CertEnumSystemStoreLocation function (wincrypt.h)

description: The CertEnumSystemStoreLocation function retrieves all of the system store locations. The function calls the provided callback function for each system store location found.
old-location: security\certenumsystemstorelocation.htm
tech.root: SecCrypto
ms.assetid: 86408e6f-0732-4cb4-85cd-840b9d98b973

ms.date: 12/05/2018
ms.keywords: CertEnumSystemStoreLocation, CertEnumSystemStoreLocation function [Security], _crypto2_certenumsystemstorelocation, security.certenumsystemstorelocation, wincrypt/CertEnumSystemStoreLocation
ms.topic: function
f1_keywords: 
 - "wincrypt/CertEnumSystemStoreLocation"
dev_langs:
 - c++
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
 - CertEnumSystemStoreLocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertEnumSystemStoreLocation function


## -description


The <b>CertEnumSystemStoreLocation</b> function retrieves all of the system store locations. The function calls the provided callback function for each system store location found.


## -parameters




### -param dwFlags [in]

Reserved for future use; must be zero.


### -param pvArg [in]

A pointer to a <b>void</b>  that allows the application to declare, define, and initialize a structure to hold any information to be passed to the callback enumeration function.


### -param pfnEnum [in]

A pointer to the callback function used to show the details for each store location. This callback function determines the content and format for the presentation of information on each store location. For the signature and parameters of the callback function, see <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location">CertEnumSystemStoreLocationCallback</a>.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.
						
						

If the function fails, it returns <b>FALSE</b>.




## -remarks



To use <b>CertEnumSystemStoreLocation</b>, an application must declare and define the <b>ENUM_ARG</b> structure and an enumeration callback function.


#### Examples

For an example that uses this function, see 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/example-c-program-listing-system-and-physical-stores">Example C Program: Listing System and Physical Stores</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certenumphysicalstore">CertEnumPhysicalStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstore">CertEnumSystemStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certregisterphysicalstore">CertRegisterPhysicalStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certregistersystemstore">CertRegisterSystemStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certunregisterphysicalstore">CertUnregisterPhysicalStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certunregistersystemstore">CertUnregisterSystemStore</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>
 

 

