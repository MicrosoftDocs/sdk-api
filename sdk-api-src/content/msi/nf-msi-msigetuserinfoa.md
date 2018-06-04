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

# MsiGetUserInfoA function


## -description


The 
<b>MsiGetUserInfo</b> function returns the registered user information for an installed product.


## -parameters




### -param szProduct [in]

Specifies the product code for the product to be queried.


### -param lpUserNameBuf [out]

Pointer to a variable that receives the name of the user.


### -param pcchUserNameBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpUserNameBuf</i> parameter. This size should include the terminating null character.


### -param lpOrgNameBuf [out]

Pointer to a buffer that receives the organization name.


### -param pcchOrgNameBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpOrgNameBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.


### -param lpSerialBuf [in]

Pointer to a buffer that receives the product ID.


### -param pcchSerialBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpSerialBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
Some or all of the user information is absent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product code does not identify a known product.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



When the 
<b>MsiGetUserInfo</b> function returns, the <i>pcchNameBuf</i> parameter contains the length of the class string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not big enough, the 
<b>MsiGetUserInfo</b> function returns USERINFOSTATE_MOREDATA, and 
<b>MsiGetUserInfo</b> contains the size of the string, in characters, without counting the null character.

The user information is considered to be present even in the absence of a company name.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

