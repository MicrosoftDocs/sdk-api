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

# _SCHANNEL_CERT_HASH structure


## -description


Contains the hash store data for the certificate that Schannel uses.


## -struct-fields




### -field dwLength

The size, in bytes, of this structure.


### -field dwFlags

Contains bit flags that control the behavior of Schannel. This member can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCH_MACHINE_CERT_HASH"></a><a id="sch_machine_cert_hash"></a><dl>
<dt><b>SCH_MACHINE_CERT_HASH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The certificate hash of the computer.

</td>
</tr>
</table>
 


### -field hProv

Handle to the cryptography provider.


### -field ShaHash

The secure hash algorithm.

