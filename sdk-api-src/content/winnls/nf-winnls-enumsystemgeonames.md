---
UID: NF:winnls.EnumSystemGeoNames
title: EnumSystemGeoNames function
author: windows-sdk-content
description: Enumerates the two-letter International Organization for Standardization (ISO) 3166-1 codes or numeric United Nations (UN) Series M, Number 49 (M.49) codes for geographical locations that are available on the operating system.
old-location: intl\enumsystemgeonames.htm
old-project: Intl
ms.assetid: 0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EnumSystemGeoNames, EnumSystemGeoNames function [Internationalization for Windows Applications], intl.enumsystemgeonames, winnls/EnumSystemGeoNames
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
 - EnumSystemGeoNames
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumSystemGeoNames function


## -description


Enumerates the two-letter International Organization for Standardization (ISO) 3166-1 codes or numeric United Nations (UN) Series M, Number 49  (M.49) codes for geographical locations that are available on the operating system.


## -parameters




### -param geoClass [in]

The geographical location class for which to enumerate the available two-letter ISO 3166-1 or numeric UN M.49 codes.


### -param geoEnumProc [in]

Pointer to the application-defined callback function <a href="https://msdn.microsoft.com/51C64387-5BDF-463B-8A93-9748C099BB09">Geo_EnumNameProc</a>. The <b>EnumSystemGeoNames</b> function calls this callback function for each of the two-letter ISO 3166-1 or numeric UN M.49 codes for geographical locations that are available on the operating system until callback function returns <b>FALSE</b>.


### -param data [in, optional]

Application-specific information to pass to the callback function that the <i>genEnumProc</i> parameter specifies.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
</table>
 




## -remarks



For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.




## -see-also




<a href="https://msdn.microsoft.com/b25d9eb3-baaa-4508-b7d6-e2bccc3c2b77">EnumSystemGeoID</a>



<a href="https://msdn.microsoft.com/51C64387-5BDF-463B-8A93-9748C099BB09">Geo_EnumNameProc</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

