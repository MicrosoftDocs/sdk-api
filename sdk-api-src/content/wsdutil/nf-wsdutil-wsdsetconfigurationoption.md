---
UID: NF:wsdutil.WSDSetConfigurationOption
title: WSDSetConfigurationOption function (wsdutil.h)
description: Sets a WSDAPI configuration option.
helpviewer_keywords: ["WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE","WSDSetConfigurationOption","WSDSetConfigurationOption function","ncd.wsdsetconfigurationoption","wsdutil/WSDSetConfigurationOption"]
old-location: ncd\wsdsetconfigurationoption.htm
tech.root: ncd
ms.assetid: d7d9b946-9f02-4770-aafe-5ee9e04a51cd
ms.date: 12/05/2018
ms.keywords: WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, WSDSetConfigurationOption, WSDSetConfigurationOption function, ncd.wsdsetconfigurationoption, wsdutil/WSDSetConfigurationOption
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
 - WSDSetConfigurationOption
 - wsdutil/WSDSetConfigurationOption
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
 - WSDSetConfigurationOption
---

# WSDSetConfigurationOption function


## -description

Sets a WSDAPI configuration option.

## -parameters

### -param dwOption

The type of configuration data to set.

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
Set the maximum size, in bytes, of an inbound message. 

</td>
</tr>
</table>

### -param pVoid [in]

Pointer to the configuration data. If <i>dwOption</i> is set to WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, then <i>pVoid</i> should point to a DWORD that represents the  size of an inbound message. The size of the message is  a value between 32768 and 1048576.

### -param cbInBuffer

The size, in bytes, of the data pointed to by <i>pVoid</i>. If <i>dwOption</i> is set to WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, this parameter should be set to <code>sizeof(DWORD)</code>.

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
The <i>dwOption</i> is not set to WSDAPI_OPTION_MAX_INBOUND_MESSAGE_SIZE, <i>cbInBuffer</i> is 0, <i>cbInBuffer</i> is not the correct size for the type of configuration data, or <i>pVoid</i> is NULL.

</td>
</tr>
</table>

