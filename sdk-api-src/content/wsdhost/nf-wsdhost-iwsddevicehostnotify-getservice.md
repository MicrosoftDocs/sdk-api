---
UID: NF:wsdhost.IWSDDeviceHostNotify.GetService
title: IWSDDeviceHostNotify::GetService (wsdhost.h)
description: Retrieves a service object that is not currently registered.
helpviewer_keywords: ["GetService","GetService method","GetService method","IWSDDeviceHostNotify interface","IWSDDeviceHostNotify interface","GetService method","IWSDDeviceHostNotify.GetService","IWSDDeviceHostNotify::GetService","ncd.iwsddevicehostnotify_getservice_method","wsdhost/IWSDDeviceHostNotify::GetService"]
old-location: ncd\iwsddevicehostnotify_getservice_method.htm
tech.root: ncd
ms.assetid: 5222b99a-b438-4775-91f0-8bcc7d3b73e8
ms.date: 12/05/2018
ms.keywords: GetService, GetService method, GetService method,IWSDDeviceHostNotify interface, IWSDDeviceHostNotify interface,GetService method, IWSDDeviceHostNotify.GetService, IWSDDeviceHostNotify::GetService, ncd.iwsddevicehostnotify_getservice_method, wsdhost/IWSDDeviceHostNotify::GetService
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
 - IWSDDeviceHostNotify::GetService
 - wsdhost/IWSDDeviceHostNotify::GetService
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
 - IWSDDeviceHostNotify.GetService
---

# IWSDDeviceHostNotify::GetService


## -description

Retrieves a service object that is not currently registered.

## -parameters

### -param pszServiceId [in]

The ID of the service to be produced.

### -param ppService [out]

 A reference to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> object for the specified service.

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
</table>

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehostnotify">IWSDDeviceHostNotify</a>