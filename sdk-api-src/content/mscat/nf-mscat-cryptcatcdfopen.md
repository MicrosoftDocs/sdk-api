---
UID: NF:mscat.CryptCATCDFOpen
title: CryptCATCDFOpen function (mscat.h)
description: Opens an existing catalog definition file (CDF) for reading and initializes a CRYPTCATCDF structure.
helpviewer_keywords: ["CryptCATCDFOpen","CryptCATCDFOpen function [Security]","mscat/CryptCATCDFOpen","security.cryptcatcdfopen"]
old-location: security\cryptcatcdfopen.htm
tech.root: security
ms.assetid: d400d8bd-c0a0-41dc-9093-8e4fc758d82f
ms.date: 12/05/2018
ms.keywords: CryptCATCDFOpen, CryptCATCDFOpen function [Security], mscat/CryptCATCDFOpen, security.cryptcatcdfopen
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
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATCDFOpen
 - mscat/CryptCATCDFOpen
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
 - CryptCATCDFOpen
---

# CryptCATCDFOpen function


## -description

<p class="CCE_Message">[The  <b>CryptCATCDFOpen</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The [CRYPTCATCDF](/windows/desktop/api/mscat/ns-mscat-cryptcatcdf) structure.   <b>CryptCATCDFOpen</b> is called by <a href="/windows/desktop/SecCrypto/makecat">MakeCat</a>.

## -parameters

### -param pwszFilePath [in]

A pointer to a null-terminated string that contains the path of the CDF file to open.

### -param pfnParseError [in, optional]

A pointer to a user-defined function to handle file parse errors.

## -returns

Upon success, this function returns a pointer to the newly created [CRYPTCATCDF](/windows/desktop/api/mscat/ns-mscat-cryptcatcdf) structure. The <b>CryptCATCDFOpen</b> function returns a <b>NULL</b> pointer if it fails.

## -remarks

The following default values are used by the <b>CryptCATCDFOpen</b> function for given conditions in the CDF <b>CatalogHeader</b> section.

<table>
<tr>
<th><b>CatalogHeader</b> condition</th>
<th>Default value</th>
</tr>
<tr>
<td>
No <b>Name</b> value is specified.

</td>
<td>
The file name in <i>pwszFilePath</i> is used for the catalog (.cat) output file.

</td>
</tr>
<tr>
<td>
No <b>PublicVersion</b> value is specified.

</td>
<td>
0x00000001

</td>
</tr>
<tr>
<td>
No <b>EncodingType</b> value is specified.

</td>
<td>
<b>PKCS_7_ASN_ENCODING</b> or <b>X509_ASN_ENCODING</b> (0x00010001)

</td>
</tr>
</table>
 

The following actions are performed by the <b>CryptCATCDFOpen</b> function for given error conditions.

<table>
<tr>
<th>Error condition</th>
<th>Action performed</th>
</tr>
<tr>
<td>
No <b>CatalogHeader</b> or <b>Name</b> tags are found in CDF.

</td>
<td>
If specified by the caller, the <b>CryptCATCDFOpen</b> function calls the function specified by <i>pfnParseError</i> and returns a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
The <b>CryptCATCDFOpen</b> function calls the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> function to get a handle to the catalog (.cat) output file, but it gets an invalid or <b>NULL</b> handle.

</td>
<td>
Calls the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatcdfclose">CryptCATCDFClose</a> function and returns a <b>NULL</b> pointer.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Additional OIDs for the Catalog branch</th>
<th>Definition</th>
</tr>
<tr>
<td>
szOID_CATALOG_LIST_MEMBER_V2

</td>
<td>
1.3.6.1.4.1.311.12.1.3

</td>
</tr>
<tr>
<td>
CAT_MEMBERINFO2_OBJID

</td>
<td>
1.3.6.1.4.1.311.12.2.3

</td>
</tr>
</table>
 

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The additional 	Catalog OIDs are not available.

## -see-also

[CRYPTCATCDF](/windows/desktop/api/mscat/ns-mscat-cryptcatcdf)



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatcdfclose">CryptCATCDFClose</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a>



<a href="/windows/desktop/SecCrypto/makecat">MakeCat</a>