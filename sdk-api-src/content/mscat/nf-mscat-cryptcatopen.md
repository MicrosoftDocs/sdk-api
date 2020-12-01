---
UID: NF:mscat.CryptCATOpen
title: CryptCATOpen function (mscat.h)
description: Opens a catalog and returns a context handle to the open catalog.
helpviewer_keywords: ["CRYPTCAT_OPEN_ALWAYS","CRYPTCAT_OPEN_CREATENEW","CRYPTCAT_VERSION_1","CRYPTCAT_VERSION_2","CryptCATOpen","CryptCATOpen function [Security]","mscat/CryptCATOpen","security.cryptcatopen"]
old-location: security\cryptcatopen.htm
tech.root: security
ms.assetid: e81f3a3d-d5b7-4266-838d-b83e331c8594
ms.date: 12/05/2018
ms.keywords: CRYPTCAT_OPEN_ALWAYS, CRYPTCAT_OPEN_CREATENEW, CRYPTCAT_VERSION_1, CRYPTCAT_VERSION_2, CryptCATOpen, CryptCATOpen function [Security], mscat/CryptCATOpen, security.cryptcatopen
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATOpen
 - mscat/CryptCATOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATOpen
---

# CryptCATOpen function


## -description

<p class="CCE_Message">[The <b>CryptCATOpen</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATOpen</b> function opens a catalog and returns a context handle to the open catalog.
<div class="alert"><b>Note</b>  Some older versions of Wintrust.lib do not contain the export information for this function. In this case, you must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters

### -param pwszFileName [in]

A pointer to a null-terminated string for the catalog file name.

### -param fdwOpenFlags [in]

Zero,  to open an existing catalog file, or a bitwise combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_ALWAYS"></a><a id="cryptcat_open_always"></a><dl>
<dt><b>CRYPTCAT_OPEN_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Opens the file, if it exists, or creates a new file, if needed.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_CREATENEW"></a><a id="cryptcat_open_createnew"></a><dl>
<dt><b>CRYPTCAT_OPEN_CREATENEW</b></dt>
</dl>
</td>
<td width="60%">
A new catalog file is created. If a previously created file exists, it is overwritten.

</td>
</tr>

<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_EXISTING"></a><a id="cryptcat_open_existing"></a><dl>
<dt><b>CRYPTCAT_OPEN_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
An existing catalog file is opened.

</td>
</tr>

<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES"></a><a id="cryptcat_open_exclude_page_hashes"></a><dl>
<dt><b>CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES</b></dt>
</dl>
</td>
<td width="60%">
An existing catalog file is opened. Exclude page hashes in SPC_INDIRECT_DATA.

</td>
</tr>

<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_INCLUDE_PAGE_HASHES"></a><a id="cryptcat_open_include_page_hashes"></a><dl>
<dt><b>CRYPTCAT_OPEN_INCLUDE_PAGE_HASHES</b></dt>
</dl>
</td>
<td width="60%">
An existing catalog file is opened. Include page hashes in SPC_INDIRECT_DATA.
The above CRYPTCAT_OPEN_EXCLUDE_PAGE_HASHES takes precedence if also set.

</td>
</tr>

<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_VERIFYSIGHASH"></a><a id="cryptcat_open_verifysighash"></a><dl>
<dt><b>CRYPTCAT_OPEN_VERIFYSIGHASH</b></dt>
</dl>
</td>
<td width="60%">
An existing catalog file is opened. Verifies the signature, not the certificates.

</td>
</tr>

<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG"></a><a id="cryptcat_open_no_content_hcryptmsg"></a><dl>
<dt><b>CRYPTCAT_OPEN_NO_CONTENT_HCRYPTMSG</b></dt>
</dl>
</td>
<td width="60%">
An existing catalog file is opened. Does CryptMsgDecode without content.

</td>
</tr>

<tr>
<td width="40%"><a id="CRYPTCAT_OPEN_SORTED"></a><a id="cryptcat_open_sorted"></a><dl>
<dt><b>CRYPTCAT_OPEN_SORTED</b></dt>
</dl>
</td>
<td width="60%">
An existing catalog file is opened. Does CertCreateContext(CERT_CREATE_CONTEXT_SORTED_FLAG).

</td>
</tr>
</table>

### -param hProv [in]

A handle to a cryptographic service provider (CSP).

### -param dwPublicVersion [in]

Version of the file. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_VERSION_1"></a><a id="cryptcat_version_1"></a><dl>
<dt><b>CRYPTCAT_VERSION_1</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
Version 1 file format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_VERSION_2"></a><a id="cryptcat_version_2"></a><dl>
<dt><b>CRYPTCAT_VERSION_2</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
Version 2 file format.

<b>Windows 8 and Windows Server 2012:  </b>Support for this value begins.

</td>
</tr>
</table>

### -param dwEncodingType [in]

Encoding type used for the file. If this value is 0, then the encoding type is set to PKCS_7_ASN_ENCODING | X509_ASN_ENCODING.

## -returns

Upon success, this function returns a handle to the open catalog. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatclose">CryptCATClose</a> function. The <b>CryptCATOpen</b> function returns INVALID_HANDLE_VALUE if it fails.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatclose">CryptCATClose</a>