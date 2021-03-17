---
UID: NF:wsdclient.IWSDMetadataExchange.GetMetadata
title: IWSDMetadataExchange::GetMetadata (wsdclient.h)
description: Retrieves metadata for an object.
helpviewer_keywords: ["GetMetadata","GetMetadata method","GetMetadata method","IWSDMetadataExchange interface","IWSDMetadataExchange interface","GetMetadata method","IWSDMetadataExchange.GetMetadata","IWSDMetadataExchange::GetMetadata","ncd.iwsdmetadataexchange_getmetadata_method","wsdclient/IWSDMetadataExchange::GetMetadata"]
old-location: ncd\iwsdmetadataexchange_getmetadata_method.htm
tech.root: ncd
ms.assetid: ab84ed56-37a5-48ff-a616-cb92dc07a8ee
ms.date: 12/05/2018
ms.keywords: GetMetadata, GetMetadata method, GetMetadata method,IWSDMetadataExchange interface, IWSDMetadataExchange interface,GetMetadata method, IWSDMetadataExchange.GetMetadata, IWSDMetadataExchange::GetMetadata, ncd.iwsdmetadataexchange_getmetadata_method, wsdclient/IWSDMetadataExchange::GetMetadata
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdclient.idl
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
 - IWSDMetadataExchange::GetMetadata
 - wsdclient/IWSDMetadataExchange::GetMetadata
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
 - IWSDMetadataExchange.GetMetadata
---

# IWSDMetadataExchange::GetMetadata


## -description

Retrieves metadata for an object.

## -parameters

### -param MetadataOut [out]

Pointer to a linked list of structures containing the requested metadata.

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
<i>MetadataOut</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdmetadataexchange">IWSDMetadataExchange</a>