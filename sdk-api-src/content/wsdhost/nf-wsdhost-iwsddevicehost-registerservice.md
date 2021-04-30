---
UID: NF:wsdhost.IWSDDeviceHost.RegisterService
title: IWSDDeviceHost::RegisterService (wsdhost.h)
description: Registers a service object for incoming requests and adds the service to the device host metadata.
helpviewer_keywords: ["IWSDDeviceHost interface","RegisterService method","IWSDDeviceHost.RegisterService","IWSDDeviceHost::RegisterService","RegisterService","RegisterService method","RegisterService method","IWSDDeviceHost interface","ncd.iwsddevicehost_registerservice_method","wsdhost/IWSDDeviceHost::RegisterService"]
old-location: ncd\iwsddevicehost_registerservice_method.htm
tech.root: ncd
ms.assetid: 8e125e72-4060-4be6-b370-b2f6b24d9da7
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,RegisterService method, IWSDDeviceHost.RegisterService, IWSDDeviceHost::RegisterService, RegisterService, RegisterService method, RegisterService method,IWSDDeviceHost interface, ncd.iwsddevicehost_registerservice_method, wsdhost/IWSDDeviceHost::RegisterService
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
 - IWSDDeviceHost::RegisterService
 - wsdhost/IWSDDeviceHost::RegisterService
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
 - IWSDDeviceHost.RegisterService
---

# IWSDDeviceHost::RegisterService


## -description

Registers a service object for incoming requests and adds the service to the device host metadata.

## -parameters

### -param pszServiceId [in]

 The ID of the service to be registered. This ID must appear in the device's service host metadata.

### -param pService [in]

The service object that will handle requests addressed to the specified service.

## -returns

Possible return values include, but are not limited to, the following:

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
<i>pszServiceId</i> is <b>NULL</b>, the length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or a service matching <i>pszServiceId</i> has already been registered.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>