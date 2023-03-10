---
UID: NS:winnt._ENCLAVE_CREATE_INFO_VBS
title: ENCLAVE_CREATE_INFO_VBS (winnt.h)
description: Contains architecture-specific information to use to create an enclave when the enclave type is ENCLAVE_TYPE_VBS, which specifies a virtualization-based security (VBS) enclave.
helpviewer_keywords: ["*PENCLAVE_CREATE_INFO_VBS","ENCLAVE_CREATE_INFO_VBS","ENCLAVE_CREATE_INFO_VBS structure","ENCLAVE_VBS_FLAG_DEBUG","PENCLAVE_CREATE_INFO_VBS","PENCLAVE_CREATE_INFO_VBS structure pointer","base.enclave_create_info_vbs","winnt/ENCLAVE_CREATE_INFO_VBS","winnt/PENCLAVE_CREATE_INFO_VBS"]
old-location: base\enclave_create_info_vbs.htm
tech.root: base
ms.assetid: 5AD6D695-92D6-47AC-A43C-D3A37D28C76C
ms.date: 12/05/2018
ms.keywords: '*PENCLAVE_CREATE_INFO_VBS, ENCLAVE_CREATE_INFO_VBS, ENCLAVE_CREATE_INFO_VBS structure, ENCLAVE_VBS_FLAG_DEBUG, PENCLAVE_CREATE_INFO_VBS, PENCLAVE_CREATE_INFO_VBS structure pointer, base.enclave_create_info_vbs, winnt/ENCLAVE_CREATE_INFO_VBS, winnt/PENCLAVE_CREATE_INFO_VBS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENCLAVE_CREATE_INFO_VBS, *PENCLAVE_CREATE_INFO_VBS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCLAVE_CREATE_INFO_VBS
 - winnt/_ENCLAVE_CREATE_INFO_VBS
 - PENCLAVE_CREATE_INFO_VBS
 - winnt/PENCLAVE_CREATE_INFO_VBS
 - ENCLAVE_CREATE_INFO_VBS
 - winnt/ENCLAVE_CREATE_INFO_VBS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - ENCLAVE_CREATE_INFO_VBS
---

# ENCLAVE_CREATE_INFO_VBS structure


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

<a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave">CreateEnclave</a>