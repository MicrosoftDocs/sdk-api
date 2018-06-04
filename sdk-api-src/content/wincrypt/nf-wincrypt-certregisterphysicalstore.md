---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CertRegisterPhysicalStore function


## -description


The <b>CertRegisterPhysicalStore</b> function adds a physical store to a registry system store collection.


## -parameters




### -param pvSystemStore [in]

The system store collection to which the physical store is added. This parameter points either to a <b>null</b>-terminated Unicode string or to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure. For information about using the structure and on adding a ServiceName or ComputerName before the system store name string, see 
<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>.


### -param dwFlags [in]

The high word of the <i>dwFlags</i> parameter specifies the location of the system store. For information about defined high-word flags and appending ServiceName, UserNames, and ComputerNames to the end of the system store name, see 
<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>. 




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
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure.

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

A pointer to a Unicode string that names the physical store to be added to the system store collection. To remove a physical store from the system store collection, call the <a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a> function.


### -param pStoreInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/ad86f388-27af-442a-a76f-f386f66296ac">CERT_PHYSICAL_STORE_INFO</a> structure that provides basic information about the physical store.


### -param pvReserved [in]

Reserved for future use and must be set to <b>NULL</b>.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.




## -see-also




<a href="https://msdn.microsoft.com/ad86f388-27af-442a-a76f-f386f66296ac">CERT_PHYSICAL_STORE_INFO</a>



<a href="https://msdn.microsoft.com/5804d565-5129-4e6d-8b3d-9bd938807740">CertEnumPhysicalStore</a>



<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>



<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>



<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>



<a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

