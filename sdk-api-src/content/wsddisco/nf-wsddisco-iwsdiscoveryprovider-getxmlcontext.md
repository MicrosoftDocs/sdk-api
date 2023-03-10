---
UID: NF:wsddisco.IWSDiscoveryProvider.GetXMLContext
title: IWSDiscoveryProvider::GetXMLContext (wsddisco.h)
description: Gets the XML context associated with this provider.
helpviewer_keywords: ["GetXMLContext","GetXMLContext method","GetXMLContext method","IWSDiscoveryProvider interface","IWSDiscoveryProvider interface","GetXMLContext method","IWSDiscoveryProvider.GetXMLContext","IWSDiscoveryProvider::GetXMLContext","ncd.iwsdiscoveryprovider_getxmlcontext","wsddisco/IWSDiscoveryProvider::GetXMLContext"]
old-location: ncd\iwsdiscoveryprovider_getxmlcontext.htm
tech.root: ncd
ms.assetid: ee2a862a-9d1d-4099-982e-259b6ab815f6
ms.date: 12/05/2018
ms.keywords: GetXMLContext, GetXMLContext method, GetXMLContext method,IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,GetXMLContext method, IWSDiscoveryProvider.GetXMLContext, IWSDiscoveryProvider::GetXMLContext, ncd.iwsdiscoveryprovider_getxmlcontext, wsddisco/IWSDiscoveryProvider::GetXMLContext
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
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
 - IWSDiscoveryProvider::GetXMLContext
 - wsddisco/IWSDiscoveryProvider::GetXMLContext
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
 - IWSDiscoveryProvider.GetXMLContext
---

# IWSDiscoveryProvider::GetXMLContext


## -description

Gets the  XML context associated with this provider.

## -parameters

### -param ppContext [out]

Pointer to a pointer variable containing the XML context.

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
<i>ppContext</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The discovery provider has not been created. Call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoveryprovider">WSDCreateDiscoveryProvider</a> to create a provider.

</td>
</tr>
</table>

## -remarks

Returns an optional context for the XML state of the transaction. If the service layer is used then this should be the context the XML namespaces and types were registered with.

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-attach">Attach</a> must be called before any other <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> method is used.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a>



<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>