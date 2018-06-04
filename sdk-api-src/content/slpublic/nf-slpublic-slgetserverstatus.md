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

# SLGetServerStatus function


## -description


Checks the server status according to the specified     
	URL and RequestType.


## -parameters




### -param pwszServerURL [in]

Type: <b>PCWSTR</b>

The URL of the server.


### -param pwszAcquisitionType [in]

Type: <b>PCWSTR</b>

The acquisition type.



#### SL_INFO_KEY_SECURE_PROCESSOR_ACTIVATION_URL (L"SPCURL")



#### SL_INFO_KEY_RIGHT_ACCOUNT_ACTIVATION_URL (L"RACURL")



#### SL_INFO_KEY_PRODUCT_KEY_ACTIVATION_URL (L"PKCURL")



#### SL_INFO_KEY_USE_LICENSE_ACTIVATION_URL (L"EULURL")



#### SL_INFO_KEY_PRODUCT_ACTIVATION_URL (L"PAURL")


### -param pwszProxyServer [in, optional]

Type: <b>PCWSTR</b>

The proxy server name. Set to <b>NULL</b> for automatic proxy discovery.


### -param wProxyPort [in, optional]

Type: <b>WORD</b>

The proxy server port. Set to 0 to use the default port.


### -param phrStatus [out]

Type: <b>HRESULT*</b>

A pointer to the server status.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

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
</table>
 




## -remarks



Callers can either pass in the URL kept by themselves or get the SKU    
	specific URL by calling the <a href="https://msdn.microsoft.com/38da608d-88c9-4e3a-84a6-5b305560191f">GetProductSkuInformation</a> function and query each     
	URL.



