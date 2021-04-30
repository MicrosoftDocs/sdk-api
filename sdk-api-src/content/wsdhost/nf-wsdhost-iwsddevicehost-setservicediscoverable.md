---
UID: NF:wsdhost.IWSDDeviceHost.SetServiceDiscoverable
title: IWSDDeviceHost::SetServiceDiscoverable (wsdhost.h)
description: Controls whether or not the service is advertised using WS-Discovery.
helpviewer_keywords: ["IWSDDeviceHost interface","SetServiceDiscoverable method","IWSDDeviceHost.SetServiceDiscoverable","IWSDDeviceHost::SetServiceDiscoverable","SetServiceDiscoverable","SetServiceDiscoverable method","SetServiceDiscoverable method","IWSDDeviceHost interface","ncd.iwsddevicehost_setservicediscoverable","wsdhost/IWSDDeviceHost::SetServiceDiscoverable"]
old-location: ncd\iwsddevicehost_setservicediscoverable.htm
tech.root: ncd
ms.assetid: 8f6aa8f6-3b7a-4d13-a052-c73f21823661
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,SetServiceDiscoverable method, IWSDDeviceHost.SetServiceDiscoverable, IWSDDeviceHost::SetServiceDiscoverable, SetServiceDiscoverable, SetServiceDiscoverable method, SetServiceDiscoverable method,IWSDDeviceHost interface, ncd.iwsddevicehost_setservicediscoverable, wsdhost/IWSDDeviceHost::SetServiceDiscoverable
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDDeviceHost::SetServiceDiscoverable
 - wsdhost/IWSDDeviceHost::SetServiceDiscoverable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.SetServiceDiscoverable
---

# IWSDDeviceHost::SetServiceDiscoverable


## -description

Controls whether or not the service is advertised
    using WS-Discovery.

## -parameters

### -param pszServiceId [in]

The ID for the service.

### -param fDiscoverable [in]

<b>TRUE</b> if the service can be found
    using WS-Discovery, <b>FALSE</b> if the service is not visible to WS-Discovery.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszServiceId</i> is <b>NULL</b>, the length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or <i>pszServiceId</i>  does not correspond to a registered service.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>