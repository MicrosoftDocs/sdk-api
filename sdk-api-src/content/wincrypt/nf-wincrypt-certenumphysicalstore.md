---
UID: NF:wincrypt.CertEnumPhysicalStore
title: CertEnumPhysicalStore function
author: windows-driver-content
description: The CertEnumPhysicalStore function retrieves the physical stores on a computer. The function calls the provided callback function for each physical store found.
old-location: security\certenumphysicalstore.htm
old-project: SecCrypto
ms.assetid: 5804d565-5129-4e6d-8b3d-9bd938807740
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CertEnumPhysicalStore, CertEnumPhysicalStore function [Security], _crypto2_certenumphysicalstore, security.certenumphysicalstore, wincrypt/CertEnumPhysicalStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertEnumPhysicalStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertEnumPhysicalStore function


## -description



			The <b>CertEnumPhysicalStore</b> function retrieves the physical stores on a computer. The function calls the provided callback function for each physical store found.


## -parameters




### -param pvSystemStore [in]

If CERT_SYSTEM_STORE_RELOCATE_FLAG is set in <i>dwFlags</i>, <i>pvSystemStore</i> points to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure that indicates both the name and the location of the system store to be enumerated. Otherwise, <i>pvSystemStore</i> is a pointer to a Unicode string that names the system store whose physical stores are to be enumerated. For information about prefixing a ServiceName or ComputerName to the system store name, see 
<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>.


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

A pointer to the callback function used to show the details for each physical store. This callback function determines the content and format for the presentation of information on each physical store. The application must provide the <a href="https://msdn.microsoft.com/0651730a-39f2-4598-a81c-d05e6d282e6c">CertEnumPhysicalStoreCallback</a> callback function.


## -returns




						If the function succeeds and another physical store was found, the return value is <b>TRUE</b>.

If the system store location only supports system stores and does not support physical stores, the function returns <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the ERROR_NOT_SUPPORTED code.

If the function fails and another physical store was not found, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To use <b>CertEnumPhysicalStore</b>, an application must declare and define the <b>ENUM_ARG</b> structure and an enumeration callback function.


#### Examples

See 
<a href="https://msdn.microsoft.com/bc4268ea-f657-4789-9d0a-6e5354508f86">Example C Program: Listing System and Physical Stores</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>



<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>



<a href="https://msdn.microsoft.com/e301c76d-cacd-441a-b925-754b07e4bfa9">CertRegisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>



<a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/958e4185-4c37-450c-abfc-91b95593227e">CertUnregisterSystemStore</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

