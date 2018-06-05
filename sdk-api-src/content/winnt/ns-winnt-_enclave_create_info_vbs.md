---
UID: NS:winnt._ENCLAVE_CREATE_INFO_VBS
title: "_ENCLAVE_CREATE_INFO_VBS"
author: windows-sdk-content
description: Contains architecture-specific information to use to create an enclave when the enclave type is ENCLAVE_TYPE_VBS, which specifies a virtualization-based security (VBS) enclave.
old-location: base\enclave_create_info_vbs.htm
old-project: Memory
ms.assetid: 5AD6D695-92D6-47AC-A43C-D3A37D28C76C
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PENCLAVE_CREATE_INFO_VBS, ENCLAVE_CREATE_INFO_VBS, ENCLAVE_CREATE_INFO_VBS structure, ENCLAVE_VBS_FLAG_DEBUG, PENCLAVE_CREATE_INFO_VBS, PENCLAVE_CREATE_INFO_VBS structure pointer, _ENCLAVE_CREATE_INFO_VBS, base.enclave_create_info_vbs, winnt/ENCLAVE_CREATE_INFO_VBS, winnt/PENCLAVE_CREATE_INFO_VBS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: ENCLAVE_CREATE_INFO_VBS, *PENCLAVE_CREATE_INFO_VBS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winnt.h
api_name:
-	ENCLAVE_CREATE_INFO_VBS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

