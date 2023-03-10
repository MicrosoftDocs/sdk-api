---
UID: NS:schannel._SecPkgContext_SupportedSignatures
title: SecPkgContext_SupportedSignatures (schannel.h)
description: Specifies the signature algorithms supported by an Schannel connection.
helpviewer_keywords: ["*PSecPkgContext_SupportedSignatures","PSecPkgContext_SupportedSignatures","PSecPkgContext_SupportedSignatures structure pointer [Security]","SecPkgContext_SupportedSignatures","SecPkgContext_SupportedSignatures structure [Security]","schannel/PSecPkgContext_SupportedSignatures","schannel/SecPkgContext_SupportedSignatures","security.secpkgcontext_supportedsignatures"]
old-location: security\secpkgcontext_supportedsignatures.htm
tech.root: security
ms.assetid: b4b58175-1367-4c91-8680-523a4b125c76
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_SupportedSignatures, PSecPkgContext_SupportedSignatures, PSecPkgContext_SupportedSignatures structure pointer [Security], SecPkgContext_SupportedSignatures, SecPkgContext_SupportedSignatures structure [Security], schannel/PSecPkgContext_SupportedSignatures, schannel/SecPkgContext_SupportedSignatures, security.secpkgcontext_supportedsignatures'
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SecPkgContext_SupportedSignatures, *PSecPkgContext_SupportedSignatures
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_SupportedSignatures
 - schannel/_SecPkgContext_SupportedSignatures
 - PSecPkgContext_SupportedSignatures
 - schannel/PSecPkgContext_SupportedSignatures
 - SecPkgContext_SupportedSignatures
 - schannel/SecPkgContext_SupportedSignatures
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
 - SecPkgContext_SupportedSignatures
---

# SecPkgContext_SupportedSignatures structure


## -description

Specifies the signature algorithms supported by an Schannel connection.

## -struct-fields

### -field cSignatureAndHashAlgorithms

The number of elements in the <i>pSignatureAndHashAlgorithms</i> array.

### -field pSignatureAndHashAlgorithms

An array of values that specify supported algorithms. These values are in the following format.


The upper byte can be one of the following values that specifies a signature algorithm.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Anonymous signature algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The RSA signature algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The DSA signature algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The ECDSA signature algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>255</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>
 


The lower byte can be one of the following values that specifies a hash algorithm.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
None.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The MD5 hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The SHA1 hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The SHA-224 hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The SHA-256 hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The SHA-384 hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The SHA-512 hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>255</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesw">QueryContextAttributes (Schannel)</a>