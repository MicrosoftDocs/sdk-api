---
UID: NF:slpublic.SLGetServerStatus
title: SLGetServerStatus function (slpublic.h)
description: Checks the server status according to the specified URL and RequestType.
helpviewer_keywords: ["SLGetServerStatus","SLGetServerStatus function [Security]","SL_INFO_KEY_PRODUCT_ACTIVATION_URL","SL_INFO_KEY_PRODUCT_KEY_ACTIVATION_URL","SL_INFO_KEY_RIGHT_ACCOUNT_ACTIVATION_URL","SL_INFO_KEY_SECURE_PROCESSOR_ACTIVATION_URL","SL_INFO_KEY_USE_LICENSE_ACTIVATION_URL","security.slgetserverstatus","slpublic/SLGetServerStatus"]
old-location: security\slgetserverstatus.htm
tech.root: security
ms.assetid: 3c07fdcc-2282-4d94-ac60-001571cd5da8
ms.date: 12/05/2018
ms.keywords: SLGetServerStatus, SLGetServerStatus function [Security], SL_INFO_KEY_PRODUCT_ACTIVATION_URL, SL_INFO_KEY_PRODUCT_KEY_ACTIVATION_URL, SL_INFO_KEY_RIGHT_ACCOUNT_ACTIVATION_URL, SL_INFO_KEY_SECURE_PROCESSOR_ACTIVATION_URL, SL_INFO_KEY_USE_LICENSE_ACTIVATION_URL, security.slgetserverstatus, slpublic/SLGetServerStatus
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLGetServerStatus
 - slpublic/SLGetServerStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetServerStatus
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
	specific URL by calling the <a href="/windows/desktop/api/slpublic/nf-slpublic-slgetproductskuinformation">GetProductSkuInformation</a> function and query each     
	URL.