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

# GetPackagesByPackageFamily function


## -description


Gets the packages  with the specified family name for the current user.




## -parameters




### -param packageFamilyName [in]

Type: <b>PCWSTR</b>

The package family name.


### -param count [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of package full names. 

First you pass <b>NULL</b> to <i>packageFullNames</i> to get the number of package full names. You use this number to allocate memory space for <i>packageFullNames</i>. Then you pass the address of this number to fill <i>packageFullNames</i>.


### -param packageFullNames [out, optional]

Type: <b>PWSTR*</b>

A pointer to the strings of package full names.


### -param bufferLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters in the string of package full names. 

First you pass <b>NULL</b> to <i>buffer</i> to get the number of characters. You use this number to allocate memory space for <i>buffer</i>. Then you pass the address of this number to fill <i>buffer</i>.


### -param buffer [out, optional]

Type: <b>WCHAR*</b>

The string of characters for all of the package full names.


## -returns



Type: <b>LONG</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

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
One or more buffer is not large enough to hold the data. The required size is specified  by either <i>count</i> or <i>buffer</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4AA5BD75-F865-40D6-9C10-E54C197D47C4">PackageNameAndPublisherIdFromFamilyName</a>
 

 

