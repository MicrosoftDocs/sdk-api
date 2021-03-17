---
UID: NF:wsdclient.IWSDEndpointProxy.ProcessFault
title: IWSDEndpointProxy::ProcessFault (wsdclient.h)
description: Processes a SOAP fault retrieved by GetFaultInfo.
helpviewer_keywords: ["IWSDEndpointProxy interface","ProcessFault method","IWSDEndpointProxy.ProcessFault","IWSDEndpointProxy::ProcessFault","ProcessFault","ProcessFault method","ProcessFault method","IWSDEndpointProxy interface","ncd.iwsdendpointproxy_processfault","wsdclient/IWSDEndpointProxy::ProcessFault"]
old-location: ncd\iwsdendpointproxy_processfault.htm
tech.root: ncd
ms.assetid: f63c8c7c-8581-49d4-a29d-a7b0b46a2db5
ms.date: 12/05/2018
ms.keywords: IWSDEndpointProxy interface,ProcessFault method, IWSDEndpointProxy.ProcessFault, IWSDEndpointProxy::ProcessFault, ProcessFault, ProcessFault method, ProcessFault method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_processfault, wsdclient/IWSDEndpointProxy::ProcessFault
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
 - IWSDEndpointProxy::ProcessFault
 - wsdclient/IWSDEndpointProxy::ProcessFault
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
 - IWSDEndpointProxy.ProcessFault
---

# IWSDEndpointProxy::ProcessFault


## -description

Processes a SOAP fault retrieved by <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsdendpointproxy-getfaultinfo">GetFaultInfo</a>.

## -parameters

### -param pFault [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a> structure containing the fault data.

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
<i>pFault</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The fault was not stored in memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a>