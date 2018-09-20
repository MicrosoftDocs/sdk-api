---
UID: NF:mscat.CryptCATCDFOpen
title: CryptCATCDFOpen function
author: windows-sdk-content
description: Opens an existing catalog definition file (CDF) for reading and initializes a CRYPTCATCDF structure.
old-location: security\cryptcatcdfopen.htm
tech.root: seccrypto
ms.assetid: d400d8bd-c0a0-41dc-9093-8e4fc758d82f
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CryptCATCDFOpen, CryptCATCDFOpen function [Security], mscat/CryptCATCDFOpen, security.cryptcatcdfopen
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATCDFOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATCDFOpen function


## -description


<p class="CCE_Message">[The  <b>CryptCATCDFOpen</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATCDFOpen</b> function opens an existing catalog definition file (CDF) for reading and initializes a <a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a> structure.   <b>CryptCATCDFOpen</b> is called by <a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>.


## -parameters




### -param pwszFilePath [in]

A pointer to a null-terminated string that contains the path of the CDF file to open.


### -param pfnParseError [in, optional]

A pointer to a user-defined function to handle file parse errors.


## -returns



Upon success, this function returns a pointer to the newly created <a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a> structure. The <b>CryptCATCDFOpen</b> function returns a <b>NULL</b> pointer if it fails.




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
The <b>CryptCATCDFOpen</b> function calls the <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> function to get a handle to the catalog (.cat) output file, but it gets an invalid or <b>NULL</b> handle.

</td>
<td>
Calls the <a href="https://msdn.microsoft.com/9f2a1175-f9fe-4f4d-bf6f-e4f4c59739ec">CryptCATCDFClose</a> function and returns a <b>NULL</b> pointer.

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




<a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a>



<a href="https://msdn.microsoft.com/9f2a1175-f9fe-4f4d-bf6f-e4f4c59739ec">CryptCATCDFClose</a>



<a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a>



<a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>
 

 

