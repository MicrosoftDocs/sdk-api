---
UID: NS:mscat.CRYPTCATSTORE_
title: CRYPTCATSTORE (mscat.h)
description: Represents a catalog file.
helpviewer_keywords: ["CRYPTCATSTORE","CRYPTCATSTORE structure [Security]","CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES","CRYPTCAT_OPEN_FLAGS_MASK","CRYPTCAT_OPEN_INCLUDE_PAGE_HASHES","CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG","CRYPTCAT_OPEN_SORTED","CRYPTCAT_OPEN_VERIFYSIGHASH","mscat/CRYPTCATSTORE","security.cryptcatstore"]
old-location: security\cryptcatstore.htm
tech.root: security
ms.assetid: 65a15797-453c-4f47-8ea1-c92e616b50aa
ms.date: 12/05/2018
ms.keywords: CRYPTCATSTORE, CRYPTCATSTORE structure [Security], CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES, CRYPTCAT_OPEN_FLAGS_MASK, CRYPTCAT_OPEN_INCLUDE_PAGE_HASHES, CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG, CRYPTCAT_OPEN_SORTED, CRYPTCAT_OPEN_VERIFYSIGHASH, mscat/CRYPTCATSTORE, security.cryptcatstore
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPTCATSTORE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CRYPTCATSTORE_
 - mscat/CRYPTCATSTORE_
 - CRYPTCATSTORE
 - mscat/CRYPTCATSTORE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mscat.h
api_name:
 - CRYPTCATSTORE
---

# CRYPTCATSTORE structure


## -description

<p class="CCE_Message">[The  <b>CRYPTCATSTORE</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

 The <b>CRYPTCATSTORE</b> structure represents a catalog file. The <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatstorefromhandle">CryptCATStoreFromHandle</a> function populates this structure by using the handle returned by <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a>.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field dwPublicVersion

A value that specifies the "PublicVersion" of the catalog file.

### -field pwszP7File

A pointer to a null-terminated string that contains the name of the catalog file. This member must be initialized before a call to the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatpersiststore">CryptCATPersistStore</a> function.

### -field hProv

A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

### -field dwEncodingType

A value that specifies the encoding type used for the file. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -field fdwStoreFlags

A bitwise combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES"></a><a id="cryptcat_open_exclude_page_hashes"></a><dl>
<dt><b>CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Exclude page hashes in SPC_INDIRECT_DATA.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_FLAGS_MASK"></a><a id="cryptcat_open_flags_mask"></a><dl>
<dt><b>CRYPTCAT_OPEN_FLAGS_MASK</b></dt>
<dt>0xffff0000</dt>
</dl>
</td>
<td width="60%">
 For all flags with a value in the upper word, set or clear the flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_INCLUDE_PAGE_HASHES"></a><a id="cryptcat_open_include_page_hashes"></a><dl>
<dt><b>CRYPTCAT_OPEN_INCLUDE_PAGE_HASHES</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Include page hashes in SPC_INDIRECT_DATA. The <b>CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES</b> flag takes precedence if it is also set.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG"></a><a id="cryptcat_open_no_content_hcryptmsg"></a><dl>
<dt><b>CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Open the file for decoding without detached content.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_SORTED"></a><a id="cryptcat_open_sorted"></a><dl>
<dt><b>CRYPTCAT_OPEN_SORTED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Open the catalog with the entries sorted alphabetically by subject.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_VERIFYSIGHASH"></a><a id="cryptcat_open_verifysighash"></a><dl>
<dt><b>CRYPTCAT_OPEN_VERIFYSIGHASH</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Verify the signature hash but not the certificate chain.

</td>
</tr>
</table>

### -field hReserved

This member is reserved and must be <b>NULL</b>.

### -field hAttrs

This member is reserved and must be <b>NULL</b>.

### -field hCryptMsg

A handle to the decoded bytes. This member is only set if the file was opened with the <b>CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG</b> flag set.

### -field hSorted

This member is reserved and must be <b>NULL</b>.