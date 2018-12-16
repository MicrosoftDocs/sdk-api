---
UID: NC:mscat.PFN_CDF_PARSE_ERROR_CALLBACK
title: PFN_CDF_PARSE_ERROR_CALLBACK
author: windows-sdk-content
description: Called for Catalog Definition Function errors while parsing a catalog definition file (CDF).
old-location: security\pfn_cdf_parse_error_callback.htm
tech.root: seccrypto
ms.assetid: 94c12ad7-dcb0-4099-8eba-da38367f0d79
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PFN_CDF_PARSE_ERROR_CALLBACK, PFN_CDF_PARSE_ERROR_CALLBACK callback, PFN_CDF_PARSE_ERROR_CALLBACK callback function [Security], mscat/PFN_CDF_PARSE_ERROR_CALLBACK, security.pfn_cdf_parse_error_callback
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mscat.h
api_name:
 - PFN_CDF_PARSE_ERROR_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CDF_PARSE_ERROR_CALLBACK callback function


## -description


The <b>PFN_CDF_PARSE_ERROR_CALLBACK</b> function is called for <a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Catalog Definition Function</a> errors while parsing a catalog definition file (CDF).


## -parameters




### -param dwErrorArea [in]

A value that indicates in which area of the CDF the error occurred.


### -param dwLocalError [in]

A value that indicates the type of error.


### -param *pwszLine [in]

A pointer to a null-terminated string that contains the CDF line in which the error occurred.


## -returns



This callback function does not return a value.




## -remarks



The <i>dwErrorArea</i> parameter can have the following possible values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>CRYPTCAT_E_AREA_HEADER</td>
<td>The header section of the CDF</td>
</tr>
<tr>
<td>CRYPTCAT_E_AREA_MEMBER</td>
<td>A member file entry in the CatalogFiles section of the CDF</td>
</tr>
<tr>
<td>CRYPTCAT_E_AREA_ATTRIBUTE</td>
<td>An attribute entry in the CDF</td>
</tr>
</table>
 

The <i>dwLocalError</i> parameter can have the following possible values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_UNSUPPORTED</td>
<td>The function does not support the attribute.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_DUPLICATE</td>
<td>The file member already exists.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_TAGNOTFOUND</td>
<td>The CatalogHeader or Name tag is missing.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_MEMBER_FILE_PATH</td>
<td>The member file name or path is missing.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_MEMBER_INDIRECTDATA</td>
<td>The function failed to create a hash of the member subject.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_MEMBER_FILENOTFOUND</td>
<td>The function failed to find the member file.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_BAD_GUID_CONV</td>
<td>The function failed to convert the subject string to a GUID.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_ATTR_TOOFEWVALUES</td>
<td>The attribute line is missing one or more elements of its composition including type, <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) or name, or value.</td>
</tr>
<tr>
<td>CRYPTCAT_E_CDF_ATTR_TYPECOMBO</td>
<td>The attribute contains an invalid OID, or the combination of type, name or OID, and value is not valid.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Catalog Definition Function</a>
 

 

