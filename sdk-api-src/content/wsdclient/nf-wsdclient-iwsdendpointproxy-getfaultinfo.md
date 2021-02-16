---
UID: NF:wsdclient.IWSDEndpointProxy.GetFaultInfo
title: IWSDEndpointProxy::GetFaultInfo (wsdclient.h)
description: Retrieves information on the last received fault.
helpviewer_keywords: ["GetFaultInfo","GetFaultInfo method","GetFaultInfo method","IWSDEndpointProxy interface","IWSDEndpointProxy interface","GetFaultInfo method","IWSDEndpointProxy.GetFaultInfo","IWSDEndpointProxy::GetFaultInfo","ncd.iwsdendpointproxy_getfaultinfo","wsdclient/IWSDEndpointProxy::GetFaultInfo"]
old-location: ncd\iwsdendpointproxy_getfaultinfo.htm
tech.root: ncd
ms.assetid: 45ed30fd-7e4f-44f5-bb90-5686746e39be
ms.date: 12/05/2018
ms.keywords: GetFaultInfo, GetFaultInfo method, GetFaultInfo method,IWSDEndpointProxy interface, IWSDEndpointProxy interface,GetFaultInfo method, IWSDEndpointProxy.GetFaultInfo, IWSDEndpointProxy::GetFaultInfo, ncd.iwsdendpointproxy_getfaultinfo, wsdclient/IWSDEndpointProxy::GetFaultInfo
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDEndpointProxy::GetFaultInfo
 - wsdclient/IWSDEndpointProxy::GetFaultInfo
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
 - IWSDEndpointProxy.GetFaultInfo
---

# IWSDEndpointProxy::GetFaultInfo


## -description

Retrieves information on the last received fault.

## -parameters

### -param ppFault [out]

Pointer to a pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a> structure containing the SOAP fault information.

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
<i>ppFault</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  The fault information returned in  <i>ppFault</i> must be released with <b>WSDFreeLinkedMemory</b> when it is no longer required for use.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a>