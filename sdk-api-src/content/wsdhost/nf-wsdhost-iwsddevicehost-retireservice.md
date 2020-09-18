---
UID: NF:wsdhost.IWSDDeviceHost.RetireService
title: IWSDDeviceHost::RetireService (wsdhost.h)
description: Unregisters a service object that was registered using RegisterService and removes the service from the device host metadata.
helpviewer_keywords: ["IWSDDeviceHost interface","RetireService method","IWSDDeviceHost.RetireService","IWSDDeviceHost::RetireService","RetireService","RetireService method","RetireService method","IWSDDeviceHost interface","ncd.iwsddevicehost_retireservice_method","wsdhost/IWSDDeviceHost::RetireService"]
old-location: ncd\iwsddevicehost_retireservice_method.htm
tech.root: ncd
ms.assetid: 7832c787-f268-44e3-b394-363299b6a823
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,RetireService method, IWSDDeviceHost.RetireService, IWSDDeviceHost::RetireService, RetireService, RetireService method, RetireService method,IWSDDeviceHost interface, ncd.iwsddevicehost_retireservice_method, wsdhost/IWSDDeviceHost::RetireService
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
 - IWSDDeviceHost::RetireService
 - wsdhost/IWSDDeviceHost::RetireService
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
 - IWSDDeviceHost.RetireService
---

# IWSDDeviceHost::RetireService


## -description

Unregisters a service object that was registered using  <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a> and removes the service from the device host metadata.

## -parameters

### -param pszServiceId [in]

The ID of the service to be removed.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszServiceId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or <i>pszServiceId</i> was not found in the list of registered services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. It may have failed because the host has not been initialized. Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-init">Init</a> to initialize a device host.

</td>
</tr>
</table>

## -remarks

The device host releases its reference to the service object after the service is unregistered. The service object will not receive callbacks after <b>RetireService</b> has completed.

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>