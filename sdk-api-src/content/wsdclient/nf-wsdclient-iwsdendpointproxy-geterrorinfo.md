---
UID: NF:wsdclient.IWSDEndpointProxy.GetErrorInfo
title: IWSDEndpointProxy::GetErrorInfo (wsdclient.h)
description: Retrieves information on the last error.
helpviewer_keywords: ["GetErrorInfo","GetErrorInfo method","GetErrorInfo method","IWSDEndpointProxy interface","IWSDEndpointProxy interface","GetErrorInfo method","IWSDEndpointProxy.GetErrorInfo","IWSDEndpointProxy::GetErrorInfo","ncd.iwsdendpointproxy_geterrorinfo","wsdclient/IWSDEndpointProxy::GetErrorInfo"]
old-location: ncd\iwsdendpointproxy_geterrorinfo.htm
tech.root: ncd
ms.assetid: 950f5634-1cc5-4981-9053-e9090374cc5e
ms.date: 12/05/2018
ms.keywords: GetErrorInfo, GetErrorInfo method, GetErrorInfo method,IWSDEndpointProxy interface, IWSDEndpointProxy interface,GetErrorInfo method, IWSDEndpointProxy.GetErrorInfo, IWSDEndpointProxy::GetErrorInfo, ncd.iwsdendpointproxy_geterrorinfo, wsdclient/IWSDEndpointProxy::GetErrorInfo
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
 - IWSDEndpointProxy::GetErrorInfo
 - wsdclient/IWSDEndpointProxy::GetErrorInfo
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
 - IWSDEndpointProxy.GetErrorInfo
---

# IWSDEndpointProxy::GetErrorInfo


## -description

Retrieves information on the last error.

## -parameters

### -param ppszErrorInfo [out]

Pointer to a buffer containing the data for the last recorded error.

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
<i>ppszErrorInfo</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  The error information returned in  <i>ppszErrorInfo</i> must be released with <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a> when it is no longer required for use.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a>