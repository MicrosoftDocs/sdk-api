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

# CRYPTCATSTORE_ structure


## -description


<p class="CCE_Message">[The  <b>CRYPTCATSTORE</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

 The <b>CRYPTCATSTORE</b> structure represents a catalog file. The <a href="https://msdn.microsoft.com/ce4fe972-0ed5-4b18-8ec5-9883af326335">CryptCATStoreFromHandle</a> function populates this structure by using the handle returned by <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a>.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field dwPublicVersion

A value that specifies the "PublicVersion" of the catalog file.


### -field pwszP7File

A pointer to a null-terminated string that contains the name of the catalog file. This member must be initialized before a call to the <a href="https://msdn.microsoft.com/2a564b0e-fcc6-4702-8173-d18df7064e53">CryptCATPersistStore</a> function.


### -field hProv

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).


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

