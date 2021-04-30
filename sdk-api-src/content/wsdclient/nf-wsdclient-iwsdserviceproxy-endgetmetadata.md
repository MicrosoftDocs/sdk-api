---
UID: NF:wsdclient.IWSDServiceProxy.EndGetMetadata
title: IWSDServiceProxy::EndGetMetadata (wsdclient.h)
description: Completes the asynchronous metadata exchange request and retrieves the service metadata from the response.
helpviewer_keywords: ["EndGetMetadata","EndGetMetadata method","EndGetMetadata method","IWSDServiceProxy interface","IWSDServiceProxy interface","EndGetMetadata method","IWSDServiceProxy.EndGetMetadata","IWSDServiceProxy::EndGetMetadata","ncd.iwsdserviceproxy_endgetmetadata","wsdclient/IWSDServiceProxy::EndGetMetadata"]
old-location: ncd\iwsdserviceproxy_endgetmetadata.htm
tech.root: ncd
ms.assetid: 6024770a-e4cb-4db1-9767-51b559fd8244
ms.date: 12/05/2018
ms.keywords: EndGetMetadata, EndGetMetadata method, EndGetMetadata method,IWSDServiceProxy interface, IWSDServiceProxy interface,EndGetMetadata method, IWSDServiceProxy.EndGetMetadata, IWSDServiceProxy::EndGetMetadata, ncd.iwsdserviceproxy_endgetmetadata, wsdclient/IWSDServiceProxy::EndGetMetadata
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
 - IWSDServiceProxy::EndGetMetadata
 - wsdclient/IWSDServiceProxy::EndGetMetadata
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
 - IWSDServiceProxy.EndGetMetadata
---

# IWSDServiceProxy::EndGetMetadata


## -description

Completes the asynchronous metadata exchange request and retrieves the service metadata from the response.

## -parameters

### -param pResult [in]

An <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> interface that represents the result of the request. Release this object when done.

### -param ppMetadata [out]

Requested metadata. For details, see <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_metadata_section_list">WSD_METADATA_SECTION_LIST</a>. Do not release this object.

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

## -remarks

<b>EndGetMetadata</b> may block until the metadata retrieval operation has completed.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a>