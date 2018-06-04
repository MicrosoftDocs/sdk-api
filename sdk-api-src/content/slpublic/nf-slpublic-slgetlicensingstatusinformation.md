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

# SLGetLicensingStatusInformation function


## -description


Gets the  licensing status of the specified application or SKU.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

Handle to the current SLC context.


### -param pAppID [in, optional]

Type: <b>const SLID*</b>

A pointer to a <b>SLID</b> that represents the application ID.
		

<table>
<tr>
<th>pAppID</th>
<th>pProductSkuId</th>
<th>Results</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get previous right consumption result.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this SKU.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get licensing status of this application.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this application/SKU.

</td>
</tr>
</table>
 


### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to a <b>SLID</b> that represents the product ID.
		

<table>
<tr>
<th>pAppID</th>
<th>pProductSkuId</th>
<th>Results</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get previous right consumption result.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this SKU.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get licensing status of this application.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this application/SKU.

</td>
</tr>
</table>
 


### -param pwszRightName [in, optional]

Type: <b>PCWSTR</b>

Must be <b>NULL</b>.


### -param pnStatusCount [out]

Type: <b>UINT*</b>

A pointer to the number of the SKU's status.


### -param ppLicensingStatus [out]

Type: <b><a href="https://msdn.microsoft.com/e7c857d9-6f63-4b1c-a562-abb158914a7d">SL_LICENSING_STATUS</a>**</b>

A pointer to the licensing status of the SKU.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_RIGHT_NOT_CONSUMED</b></dt>
<dt>0xC004F002</dt>
</dl>
</td>
<td width="60%">
The rights consumption failed.

</td>
</tr>
</table>
 



