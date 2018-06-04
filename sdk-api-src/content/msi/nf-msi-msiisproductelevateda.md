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

# MsiIsProductElevatedA function


## -description


The <b>MsiIsProductElevated</b> function returns whether or not the product is managed. Only applications that require elevated privileges for installation and being installed through advertisement are considered managed, which means that an application installed per-machine is always considered managed. 

An application that is installed  per-user is only considered managed if it is advertised by a local system process that is impersonating the user. For more information, see <a href="https://msdn.microsoft.com/0d2bd2d9-0eac-4519-862c-15f0ee5cbc40">Advertising a Per-User Application to be Installed with Elevated Privileges</a>.
     

<b>MsiIsProductElevated</b> verifies that the local system owns the product registry data. The function does not refer to account policies such as <a href="https://msdn.microsoft.com/0bbec06a-0a2b-430a-a361-317a319da615">AlwaysInstallElevated</a>.


## -parameters




### -param szProduct

TBD


### -param pfElevated [out]

A pointer to a BOOL for the result. 

This parameter cannot be <b>NULL</b>.


#### - szProductCode [in]

The full product code GUID of the product. 

This parameter is required and cannot be <b>NULL</b> or empty.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS, and <i>pfElevated</i> is set to <b>TRUE</b> if the product is a managed application.

If the function fails, the return value is one of the error codes identified in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product is not currently known.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration information for the product is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
The function is not available for a specific platform. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/162bda20-0c62-4eac-8c1f-fd107e42c528">Determining Installation Context</a>



<a href="https://msdn.microsoft.com/61b9297e-f45e-4f50-9001-9bae580e1bf4">Installing a Package with Elevated Privileges for a Non-Admin</a>
 

 

