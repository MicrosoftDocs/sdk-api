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

# CryptCATGetAttrInfo function


## -description


<p class="CCE_Message">[The <b>CryptCATGetAttrInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATGetAttrInfo</b> function retrieves information about an attribute of a member of a catalog.


## -parameters




### -param hCatalog [in]

The handle of the catalog that contains the member to retrieve the attribute information for. This handle is obtained by calling the <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> function. This parameter is required and cannot be <b>NULL</b>.


### -param pCatMember [in]

A pointer to a <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that represents the member to retrieve the attribute information for. This can be obtained by calling the <a href="https://msdn.microsoft.com/ff265232-f57e-4ab0-ba07-05e6d6745ae3">CryptCATGetMemberInfo</a> function. This parameter is required and cannot be <b>NULL</b>.


### -param pwszReferenceTag [in]

A pointer to a null-terminated Unicode string that contains the name of the attribute to retrieve the information for. This parameter is required and cannot be <b>NULL</b>.


## -returns



This function returns a pointer to a <a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a> structure that contains the attribute information. If the function fails, it returns <b>NULL</b>.


<div class="alert"><b>Important</b>  Do not free the returned pointer nor any of the members pointed to by the returned pointer.</div>
<div> </div>



If this function returns <b>NULL</b>, additional error information can be obtained by calling the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The member or the attribute could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a>



<a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a>



<a href="https://msdn.microsoft.com/ff265232-f57e-4ab0-ba07-05e6d6745ae3">CryptCATGetMemberInfo</a>



<a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a>
 

 

