---
UID: NF:winnls.GetGeoInfoEx
title: GetGeoInfoEx function
author: windows-driver-content
description: Retrieves information about a geographic location that you specify by using a two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49 (M.49) code.
old-location: intl\getgeoinfoex.htm
old-project: Intl
ms.assetid: 05BF6434-A80F-4BF5-9A43-C4D65E72F43B
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetGeoInfoEx, GetGeoInfoEx function [Internationalization for Windows Applications], intl.getgeoinfoex, winnls/GetGeoInfoEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	GetGeoInfoEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetGeoInfoEx function


## -description


Retrieves information about a geographic location that you specify by using a two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code.


## -parameters




### -param location [in]

The two-letter ISO 3166-1 or numeric UN M.49 code for the geographic location for which to get information.  To get the codes that are available on the operating system, call <a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>.


### -param geoType [in]

The type of information you want to retrieve. Possible values are defined by the <a href="https://msdn.microsoft.com/f72f5cc5-4709-408f-a50c-b4b3092c4419">SYSGEOTYPE</a> enumeration. The following values of the <b>SYSGEOTYPE</b> enumeration should not be used with <b>GetGeoInfoEx</b>:

<ul>
<li>
<b>GEO_ID</b>

This value is provided for backward compatibility.  Do not use this value in new applications, but use <b>GEO_NAME</b> instead.

</li>
<li>
<b>GEO_LCID</b>

This value is not supported for the <b>GetGeoInfoEx</b> function.

</li>
<li>
<b>GEO_NATION</b>

This value is not supported for the <b>GetGeoInfoEx</b> function.

</li>
<li>
<b>GEO_RFC1766</b>

This value is not supported for the <b>GetGeoInfoEx</b> function.

</li>
</ul>

### -param geoData [out, optional]

A pointer to the buffer in which <b>GetGeoInfoEx</b> should write the  requested information.


### -param geoDataCount [in]

The size of the buffer to which the <i>GeoData</i> parameter points, in characters. Set this parameter to 0 to specify that the function should only return the size of the buffer required to store the requested information without writing the requested information to the buffer.


## -returns



The number of bytes of geographical location information that the function wrote the output buffer. If <i>geoDataCount</i> is  0, the function returns the size of the buffer required to hold the information without writing the information to the buffer.

0 indicates that the function did not succeed. To get extended error information,  call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The values supplied for flags were not valid.

</td>
</tr>
</table>
 




## -remarks



For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.




## -see-also




<a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>



<a href="https://msdn.microsoft.com/73827ed9-bdc5-4b34-b849-fb44b3c5bd6e">GetGeoInfo</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/f72f5cc5-4709-408f-a50c-b4b3092c4419">SYSGEOTYPE</a>
 

 

