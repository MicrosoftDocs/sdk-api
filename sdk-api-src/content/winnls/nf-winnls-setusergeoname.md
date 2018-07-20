---
UID: NF:winnls.SetUserGeoName
title: SetUserGeoName function
author: windows-sdk-content
description: Sets the geographic location for the current user to the specified two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49 (M.49) code.
old-location: intl\setusergeoname.htm
old-project: Intl
ms.assetid: 0E5934DE-F526-45B4-9DAF-C8941F00C162
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: SetUserGeoName, SetUserGeoName function [Internationalization for Windows Applications], intl.setusergeoname, winnls/SetUserGeoName
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
 - SetUserGeoName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetUserGeoName function


## -description


Sets the geographic location for the current user to the specified two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code.


## -parameters




### -param geoName [in]

The two-letter ISO 3166-1 or numeric UN M.49 code for the geographic location to set for the current user. To get the codes that are available on the operating system, call <a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

If this function does not succeed, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The group policy of the computer or the user has forbidden this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred in the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value was invalid.

</td>
</tr>
</table>
 




## -remarks



This function writes to the registry the geographical location for a particular user instead of a particular application. This action affects the behavior of other applications that the user runs. As a rule, call this function only when the user has explicitly requested changes, but not for purely application-specific reasons.

For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.

<b>SetUserGeoName</b> is intended for use by applications that are designed to change user settings, such as the Windows Settings app. Other applications should not call this function.




## -see-also




<a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>



<a href="https://msdn.microsoft.com/7938A5A1-E18E-4643-A07C-3354B4E94B5D">GetUserDefaultGeoName</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/2e201a7e-6767-4908-b98c-f5b7f0544e60">SetUserGeoID</a>
 

 

