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

# SLActivateProduct function


## -description


Acquires a use license from the Software License Server (SLS).


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pProductSkuId [in]

Type: <b>const SLID*</b>

 A pointer to the product ID.


### -param cbAppSpecificData [in, optional]

Type: <b>UINT</b>

The size of application specific data.


### -param pvAppSpecificData [in, optional]

Type: <b>const PVOID</b>

A pointer to application specific data. The license server can use this     
		information to embed application specific run-time information.


### -param pActivationInfo [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8209652d-c40e-419b-9929-647f03fed79c">SL_ACTIVATION_INFO_HEADER</a>*</b>

A pointer to additional product activation information.


### -param pwszProxyServer [in, optional]

Type: <b>PCWSTR</b>

The proxy server name. Set this to <b>NULL</b> to use automatic proxy discovery.


### -param wProxyPort [in, optional]

Type: <b>WORD</b>

The proxy server port. To use the default port, set <i>wProxyPort</i> to 0.


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
<dt><b>SL_E_PUBLISHING_LICENSE_NOT_INSTALLED</b></dt>
<dt>0xC004F017</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PKEY_NOT_INSTALLED</b></dt>
<dt>0xC004F014
</dt>
</dl>
</td>
<td width="60%">
The product key is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PRODUCT_SKU_NOT_INSTALLED</b></dt>
<dt>0xc004f015</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
</table>
 



