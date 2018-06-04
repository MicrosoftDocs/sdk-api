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

# MsiEnumProductsW function


## -description


The 
<b>MsiEnumProducts</b> function enumerates through all the products currently advertised or installed. Products that are installed in both the per-user and per-machine <a href="https://msdn.microsoft.com/20e7be9f-d9dc-4f43-86d7-b1a881126925">installation context</a> and advertisements are enumerated.


## -parameters




### -param iProductIndex [in]

Specifies the index of the product to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumProducts</b> function and then incremented for subsequent calls. Because products are not ordered, any new product has an arbitrary index. This means that the function can return products in any order.


### -param lpProductBuf [out]

Pointer to a buffer that receives the product code. This buffer must be 39 characters long. The first 38 characters are for the GUID, and the last character is for the terminating null character.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no products to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
</table>
 




## -remarks



To enumerate products, an application should initially call the 
<b>MsiEnumProducts</b> function with the <i>iProductIndex</i> parameter set to zero. The application should then increment the <i>iProductIndex</i> parameter and call 
<b>MsiEnumProducts</b> until there are no more products (until the function returns ERROR_NO_MORE_ITEMS).

When making multiple calls to 
<b>MsiEnumProducts</b> to enumerate all of the products, each call should be made from the same thread.




## -see-also




<a href="https://msdn.microsoft.com/162bda20-0c62-4eac-8c1f-fd107e42c528">Determining Installation Context</a>



<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

