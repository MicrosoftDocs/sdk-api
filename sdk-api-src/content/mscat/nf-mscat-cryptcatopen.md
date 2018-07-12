---
UID: NF:mscat.CryptCATOpen
title: CryptCATOpen function
author: windows-sdk-content
description: Opens a catalog and returns a context handle to the open catalog.
old-location: security\cryptcatopen.htm
old-project: seccrypto
ms.assetid: e81f3a3d-d5b7-4266-838d-b83e331c8594
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CRYPTCAT_OPEN_ALWAYS, CRYPTCAT_OPEN_CREATENEW, CRYPTCAT_VERSION_1, CRYPTCAT_VERSION_2, CryptCATOpen, CryptCATOpen function [Security], mscat/CryptCATOpen, security.cryptcatopen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATOpen
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATOpen function


## -description


<p class="CCE_Message">[The <b>CryptCATOpen</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATOpen</b> function opens a catalog and returns a context handle to the open catalog.
<div class="alert"><b>Note</b>  Some older versions of Wintrust.lib do not contain the export information for this function. In this case, you must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

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



Upon success, this function returns a handle to the open catalog. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/f6fa2d10-0049-4d5e-9688-566e5c11d64e">CryptCATClose</a> function. The <b>CryptCATOpen</b> function returns INVALID_HANDLE_VALUE if it fails.




## -see-also




<a href="https://msdn.microsoft.com/f6fa2d10-0049-4d5e-9688-566e5c11d64e">CryptCATClose</a>
 

 

