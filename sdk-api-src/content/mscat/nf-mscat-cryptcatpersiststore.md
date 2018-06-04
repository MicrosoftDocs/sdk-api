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

# CryptCATPersistStore function


## -description


<p class="CCE_Message">[The  <b>CryptCATPersistStore</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATPersistStore</b> function saves the information in the specified catalog store to an unsigned catalog file.


## -parameters




### -param hCatalog [in]

A handle to the catalog obtained from <a href="https://msdn.microsoft.com/e9aedc2d-9492-4ed7-9f2d-891997f85f6f">CryptCATHandleFromStore</a> or <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> function.   Beginning with Windows 8 you must use only <b>CryptCATOpen</b> to retrieve a handle.


## -returns



The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.


If this function returns <b>FALSE</b>, additional error information can be obtained by calling the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. <b>GetLastError</b> will return the following error code.



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
One or more of the parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_NOT_SUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
Beginning with Windows 8 and Windows Server 2012, you must retrieve a handle by calling the  <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> function with the <i>dwPublicVersion</i> parameter set to 0x100 or 0x200. For more information, see Remarks.

</td>
</tr>
</table>
 




## -remarks



The <b>pwszP7File</b> member of the <a href="https://msdn.microsoft.com/65a15797-453c-4f47-8ea1-c92e616b50aa">CRYPTCATSTORE</a>  structure must be initialized before you call <b>CryptCATPersistStore</b>.

Beginning with Windows 8 and Windows Server 2012, the following changes apply to this function:

<ul>
<li>If <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> was called with a <i>dwPublicVersion</i> parameter of 0x200, the catalog is written by using the v2 format.</li>
<li>If <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> was called with a <i>dwPublicVersion</i> parameter of 0x100, the catalog is written by using the v1 format.</li>
<li>If <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> was called with a <i>dwPublicVersion</i> parameter other than 0x200 or 0x100, the <b>CryptCATPersistStore</b> function returns <b>FALSE</b> and the error code is set to <b>ERROR_NOT_SUPPORTED</b>.</li>
</ul>


