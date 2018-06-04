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

# VBS_ENCLAVE_REPORT_VARDATA_HEADER structure


## -description


Describes the format of a variable data block contained in a report that the <a href="https://msdn.microsoft.com/FEE8F05B-540F-4C10-A90C-55607A4E9293">EnclaveGetAttestationReport</a> function generates.


## -struct-fields




### -field DataType

The type of the variable data block.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VBS_ENCLAVE_VARDATA_INVALID"></a><a id="vbs_enclave_vardata_invalid"></a><dl>
<dt><b>VBS_ENCLAVE_VARDATA_INVALID</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The variable data block is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="VBS_ENCLAVE_VARDATA_MODULE"></a><a id="vbs_enclave_vardata_module"></a><dl>
<dt><b>VBS_ENCLAVE_VARDATA_MODULE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The variable data block is a module.

</td>
</tr>
</table>
 


### -field Size

The size of this variable data block, including the header, in bytes.


## -remarks



An enclave attestation report includes zero or  variable data blocks. These variable data blocks consist of the following items:

<ul>
<li>A <b>VBS_ENCLAVE_REPORT_VARDATA_HEADER</b> structure that describes the format of the variable data block. </li>
<li>The data described by the <b>VBS_ENCLAVE_REPORT_VARDATA_HEADER</b> structure. If the value of the <b>DataType</b> member of the <b>VBS_ENCLAVE_REPORT_VARDATA_HEADER</b> structure is  <b>VBS_ENCLAVE_VARDATA_MODULE</b>, this data is a <a href="https://msdn.microsoft.com/FB72B01D-B3FE-4FD7-8766-B209C6BC105E">VBS_ENCLAVE_REPORT_MODULE</a> structure.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/FEE8F05B-540F-4C10-A90C-55607A4E9293">EnclaveGetAttestationReport</a>



<a href="https://msdn.microsoft.com/90D6E8D2-191B-41D2-8C75-28A26462644B">VBS_ENCLAVE_REPORT</a>



<a href="https://msdn.microsoft.com/FB72B01D-B3FE-4FD7-8766-B209C6BC105E">VBS_ENCLAVE_REPORT_MODULE</a>
 

 

