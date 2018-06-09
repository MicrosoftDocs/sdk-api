---
UID: NF:winnls.GetUserDefaultGeoName
title: GetUserDefaultGeoName function
author: windows-sdk-content
description: Retrieves the two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49 (M.49) code for the default geographical location of the user.
old-location: intl\getuserdefaultgeoname.htm
old-project: Intl
ms.assetid: 7938A5A1-E18E-4643-A07C-3354B4E94B5D
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetUserDefaultGeoName, GetUserDefaultGeoName function [Internationalization for Windows Applications], intl.getuserdefaultgeoname, winnls/GetUserDefaultGeoName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetUserDefaultGeoName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetUserDefaultGeoName function


## -description


Retrieves the two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code for the default geographical location of the user.


## -parameters




### -param geoName [out]

Pointer to a buffer in which this function should write the null-terminated two-letter ISO 3166-1 or numeric UN M.49 code for the default geographic location of the user.


### -param geoNameCount

TBD




#### - int [in]

The size of the buffer that the <i>geoName</i> parameter specifies. If this value is zero, the function only returns the number of characters that function would copy to the output buffer, but does not write the name of the default geographic location of the user to the buffer.


## -returns



The number of characters
  the function  would copy to the output buffer, if the value of the <i>geoNameCount</i> parameter is zero. Otherwise, the  number of characters that the function copied to the buffer that the <i>geoName</i> parameter specifies.

Zero indicates that the function failed. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>ERROR_BADDB</b></dt>
</dl>
</td>
<td width="60%">
The function could not read information from the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer that the  <i>geoName</i> parameter specifies is too small for the string. 

</td>
</tr>
</table>
 




## -remarks



For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.




## -see-also




<a href="https://msdn.microsoft.com/9d4d196d-4000-4866-a4c7-e7b9cb669c6f">GetUserGeoID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/0E5934DE-F526-45B4-9DAF-C8941F00C162">SetUserGeoName</a>
 

 

