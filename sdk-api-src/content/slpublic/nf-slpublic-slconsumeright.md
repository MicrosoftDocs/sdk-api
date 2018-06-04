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

# SLConsumeRight function


## -description


Let an application to exercise rights on a locally-stored licenses. Calling this function binds a license to the right.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pAppId [in]

Type: <b>const SLID*</b>

A pointer to the identifier of the application who's right is going to be          
		consumed.


### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to the identifier of product SKU. If set to <b>NULL</b>, all of the  product  SKU's          
		licenses will be consumed.


### -param pwszRightName [in, optional]

Type: <b>PCWSTR</b>

The name of right to be consumed.


### -param pvReserved

Type: <b>PVOID</b>

Reserved.


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
<dt><b>SL_E_RIGHT_NOT_GRANTED</b></dt>
<dt>0xC004F013</dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to run the software.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PRODUCT_SKU_NOT_INSTALLED </b></dt>
<dt>0xC004F015</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
</table>
 



