---
UID: NS:schannel._SCHANNEL_CERT_HASH_STORE
title: SCHANNEL_CERT_HASH_STORE (schannel.h)
description: Contains the hash store data for the certificate that Schannel uses in kernel-mode.
helpviewer_keywords: ["*PSCHANNEL_CERT_HASH_STORE","PSCHANNEL_CERT_HASH_STORE","PSCHANNEL_CERT_HASH_STORE structure pointer [Security]","SCHANNEL_CERT_HASH_STORE","SCHANNEL_CERT_HASH_STORE structure [Security]","SCH_MACHINE_CERT_HASH","schannel/PSCHANNEL_CERT_HASH_STORE","schannel/SCHANNEL_CERT_HASH_STORE","security.schannel_cert_hash_store"]
old-location: security\schannel_cert_hash_store.htm
tech.root: security
ms.assetid: 26902BD9-9426-4061-AC70-67A4F4063511
ms.date: 12/05/2018
ms.keywords: '*PSCHANNEL_CERT_HASH_STORE, PSCHANNEL_CERT_HASH_STORE, PSCHANNEL_CERT_HASH_STORE structure pointer [Security], SCHANNEL_CERT_HASH_STORE, SCHANNEL_CERT_HASH_STORE structure [Security], SCH_MACHINE_CERT_HASH, schannel/PSCHANNEL_CERT_HASH_STORE, schannel/SCHANNEL_CERT_HASH_STORE, security.schannel_cert_hash_store'
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
targetos: Windows
req.typenames: SCHANNEL_CERT_HASH_STORE, *PSCHANNEL_CERT_HASH_STORE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHANNEL_CERT_HASH_STORE
 - schannel/_SCHANNEL_CERT_HASH_STORE
 - PSCHANNEL_CERT_HASH_STORE
 - schannel/PSCHANNEL_CERT_HASH_STORE
 - SCHANNEL_CERT_HASH_STORE
 - schannel/SCHANNEL_CERT_HASH_STORE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SCHANNEL_CERT_HASH_STORE
---

# SCHANNEL_CERT_HASH_STORE structure


## -description

Contains the hash store data for the certificate that Schannel uses in kernel-mode.

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

### -field pwszStoreName

Pointer to the size of the store name.

