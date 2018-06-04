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

# MsiEnumRelatedProductsW function


## -description


The 
<b>MsiEnumRelatedProducts</b> function enumerates products with a specified upgrade code. This function lists the currently installed and advertised products that have the specified 
<a href="https://msdn.microsoft.com/6cdee5d8-8aa0-4fad-9338-152ee33b8077">UpgradeCode</a> property in their 
<a href="https://msdn.microsoft.com/1f4215b2-dc71-4e6e-bc2e-3b43316806b9">Property table</a>.


## -parameters




### -param lpUpgradeCode [in]

The null-terminated string specifying the upgrade code of related products that the installer is to enumerate.


### -param dwReserved [in]

This parameter is reserved and must be 0.


### -param iProductIndex [in]

The zero-based index into the registered products.


### -param lpProductBuf [out]

A buffer to receive the product code GUID. This buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character.


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
The system does not have enough memory to complete the operation. Available starting with Windows Server 2003.

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



See 
<a href="https://msdn.microsoft.com/6cdee5d8-8aa0-4fad-9338-152ee33b8077">UpgradeCode</a> property.

To enumerate currently installed and advertised products that have a specific upgrade code, an application should initially call the 
<b>MsiEnumRelatedProducts</b> function with the <i>iProductIndex</i> parameter set to zero. The application should then increment the <i>iProductIndex</i> parameter and call 
<b>MsiEnumRelatedProducts</b> until the function returns ERROR_NO_MORE_ITEMS, which means there are no more products with the specified upgrade code.

When making multiple calls to 
<b>MsiEnumRelatedProducts</b> to enumerate all of the related products, each call should be made from the same thread.



