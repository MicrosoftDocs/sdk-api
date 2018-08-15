---
UID: NC:wincrypt.PFN_CERT_ENUM_PHYSICAL_STORE
title: PFN_CERT_ENUM_PHYSICAL_STORE
author: windows-sdk-content
description: The CertEnumPhysicalStoreCallback callback function formats and presents information on each physical store found by a call to CertEnumPhysicalStore.
old-location: security\certenumphysicalstorecallback.htm
old-project: seccrypto
ms.assetid: 0651730a-39f2-4598-a81c-d05e6d282e6c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CertEnumPhysicalStoreCallback, CertEnumPhysicalStoreCallback callback, CertEnumPhysicalStoreCallback callback function [Security], PFN_CERT_ENUM_PHYSICAL_STORE, PFN_CERT_ENUM_PHYSICAL_STORE callback function [Security], security.certenumphysicalstorecallback, wincrypt/CertEnumPhysicalStoreCallback, wincrypt/PFN_CERT_ENUM_PHYSICAL_STORE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CertEnumPhysicalStoreCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_CERT_ENUM_PHYSICAL_STORE callback function


## -description


The <b>CertEnumPhysicalStoreCallback</b> 
    callback function formats and presents information on each physical store found by a call to 
    <a href="https://msdn.microsoft.com/5804d565-5129-4e6d-8b3d-9bd938807740">CertEnumPhysicalStore</a>.


## -parameters




### -param *pvSystemStore [in]

If CERT_SYSTEM_STORE_RELOCATE_FLAG is set in <i>dwFlags</i>, <i>pvSystemStore</i> points to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure that indicates both the name and the location of the system store to be enumerated. Otherwise, <i>pvSystemStore</i> is a pointer to a Unicode string that names the system store whose physical stores are to be enumerated. For information about prefixing the name of a service or computer to the system store name, see 
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
In addition, CERT_SYSTEM_STORE_RELOCATE_FLAG or CERT_PHYSICAL_STORE_PREDEFINED_ENUM_FLAG can be combined using a bitwise-<b>OR</b> operation with any of the high-word location flags. The CERT_PHYSICAL_STORE_PREDEFINED_ENUM_FLAG constant is set if the physical store is predefined rather than registered.


### -param pwszStoreName [in]

Name of the physical store.


### -param pStoreInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/ad86f388-27af-442a-a76f-f386f66296ac">CERT_PHYSICAL_STORE_INFO</a> structure containing information about the store.


### -param *pvReserved [in]

Reserved for future use.


### -param *pvArg [in]

A pointer to information passed to the callback function in the <i>pvArg</i> passed to <a href="https://msdn.microsoft.com/5804d565-5129-4e6d-8b3d-9bd938807740">CertEnumPhysicalStore</a>.


## -returns



Returns <b>TRUE</b> if the function succeeds, <b>FALSE</b> if it fails.




## -see-also




<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>



<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>



<a href="https://msdn.microsoft.com/e301c76d-cacd-441a-b925-754b07e4bfa9">CertRegisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>



<a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/958e4185-4c37-450c-abfc-91b95593227e">CertUnregisterSystemStore</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Store Functions</a>
 

 

