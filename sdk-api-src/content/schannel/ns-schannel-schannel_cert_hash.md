---
UID: NS:schannel._SCHANNEL_CERT_HASH
title: SCHANNEL_CERT_HASH (schannel.h)
author: windows-sdk-content
description: Contains the hash store data for the certificate that Schannel uses.
old-location: security\schannel_cert_hash.htm
tech.root: SecAuthN
ms.assetid: BC068062-6644-4296-990F-7C533DC80C02
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSCHANNEL_CERT_HASH, PSCHANNEL_CERT_HASH, PSCHANNEL_CERT_HASH structure pointer [Security], SCHANNEL_CERT_HASH, SCHANNEL_CERT_HASH structure [Security], SCH_MACHINE_CERT_HASH, schannel/PSCHANNEL_CERT_HASH, schannel/SCHANNEL_CERT_HASH, security.schannel_cert_hash"
ms.topic: struct
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SCHANNEL_CERT_HASH
product: Windows
targetos: Windows
req.typenames: SCHANNEL_CERT_HASH, *PSCHANNEL_CERT_HASH
req.redist: 
---

# SCHANNEL_CERT_HASH structure


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

