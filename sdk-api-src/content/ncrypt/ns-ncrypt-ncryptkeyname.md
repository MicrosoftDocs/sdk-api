---
UID: NS:ncrypt.NCryptKeyName
title: NCryptKeyName
author: windows-sdk-content
description: Used to contain information about a CNG key.
old-location: security\ncryptkeyname_struct.htm
tech.root: SecCNG
ms.assetid: 9d9ebbb7-c491-49b0-9686-e37085929271
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, NCRYPT_MACHINE_KEY_FLAG, NCryptKeyName, NCryptKeyName structure [Security], ncrypt/NCryptKeyName, security.ncryptkeyname_struct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - Ncrypt.h
api_name:
 - NCryptKeyName
product: Windows
targetos: Windows
req.typenames: NCryptKeyName
req.redist: 
---

# NCryptKeyName structure


## -description


The <b>NCryptKeyName</b> structure is used to contain information about a CNG key.


## -struct-fields




### -field pszName

A pointer to a null-terminated Unicode string that contains the name of the key.


### -field pszAlgid

A pointer to a null-terminated Unicode string that contains the identifier of the cryptographic algorithm that the key was created with. This can be one of the standard <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.


### -field dwLegacyKeySpec

A legacy identifier that specifies the type of key. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
The key is a key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The key is a signature key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The key is none of the above types.

</td>
</tr>
</table>
 


### -field dwFlags

A set of flags that provide more information about the key. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_MACHINE_KEY_FLAG"></a><a id="ncrypt_machine_key_flag"></a><dl>
<dt><b>NCRYPT_MACHINE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The key applies to the local computer. If this flag is not present, the key applies to the current user.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/ca8c5b70-ea5e-4fb9-82d3-1de839f0d244">NCryptEnumKeys</a>
 

 

