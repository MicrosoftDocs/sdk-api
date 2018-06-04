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

# _ENCLAVE_CREATE_INFO_VBS structure


## -description


Contains architecture-specific information to use to create an enclave when the enclave type is <b>ENCLAVE_TYPE_VBS</b>, which specifies a virtualization-based security (VBS) enclave.


## -struct-fields




### -field Flags

A flag that indicates whether the enclave permits debugging.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_VBS_FLAG_DEBUG"></a><a id="enclave_vbs_flag_debug"></a><dl>
<dt><b>ENCLAVE_VBS_FLAG_DEBUG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The enclave permits debugging.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The enclave does not permit debugging.

</td>
</tr>
</table>
 


### -field OwnerID

The identifier of the owner of the enclave.


## -see-also




<a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>
 

 

