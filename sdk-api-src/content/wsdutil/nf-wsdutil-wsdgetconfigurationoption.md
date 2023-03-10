---
UID: NF:wsdutil.WSDGetConfigurationOption
title: WSDGetConfigurationOption function (wsdutil.h)
description: Gets a WSDAPI configuration option.
helpviewer_keywords: ["WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE","WSDGetConfigurationOption","WSDGetConfigurationOption function","ncd.wsdgetconfigurationoption","wsdutil/WSDGetConfigurationOption"]
old-location: ncd\wsdgetconfigurationoption.htm
tech.root: ncd
ms.assetid: 33fc271e-4cc5-466c-8688-7b19f4399f8e
ms.date: 12/05/2018
ms.keywords: WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, WSDGetConfigurationOption, WSDGetConfigurationOption function, ncd.wsdgetconfigurationoption, wsdutil/WSDGetConfigurationOption
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDGetConfigurationOption
 - wsdutil/WSDGetConfigurationOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDGetConfigurationOption
---

# WSDGetConfigurationOption function


## -description

Gets a WSDAPI configuration option.

## -parameters

### -param dwOption

The type of configuration data to get.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE"></a><a id="wsdapi_option_max_inbound_message_size"></a><dl>
<dt><b>WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Get the maximum size, in bytes, of an inbound message. This message size is  a value between 32768 and 1048576.

</td>
</tr>
</table>

### -param pVoid [out]

Pointer to the configuration data.

### -param cbOutBuffer

The size, in bytes, of the data pointed to by <i>pVoid</i>. If <i>dwOption</i> is set to WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, then this parameter should be set to <code>sizeof(DWORD)</code>.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwOption</i> is not set to WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, <i>cbOutBuffer</i> is 0, or <i>cbOutBuffer</i> is not the correct size for the type of configuration data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pVoid</i> is <b>NULL</b>.

</td>
</tr>
</table>

