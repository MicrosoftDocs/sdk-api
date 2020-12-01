---
UID: NF:wsdattachment.WSDCreateOutboundAttachment
title: WSDCreateOutboundAttachment function (wsdattachment.h)
description: Creates an IWSDOutboundAttachment object.
helpviewer_keywords: ["WSDCreateOutboundAttachment","WSDCreateOutboundAttachment function","ncd.wsdcreateoutboundattachment","wsdattachment/WSDCreateOutboundAttachment"]
old-location: ncd\wsdcreateoutboundattachment.htm
tech.root: ncd
ms.assetid: 92e4ed8a-4a17-49dd-9ed8-bc867ec8bba9
ms.date: 12/05/2018
ms.keywords: WSDCreateOutboundAttachment, WSDCreateOutboundAttachment function, ncd.wsdcreateoutboundattachment, wsdattachment/WSDCreateOutboundAttachment
req.header: wsdattachment.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDCreateOutboundAttachment
 - wsdattachment/WSDCreateOutboundAttachment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateOutboundAttachment
---

# WSDCreateOutboundAttachment function


## -description

Creates an <a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdoutboundattachment">IWSDOutboundAttachment</a> object.

## -parameters

### -param ppAttachment [out]

Returns a reference to the initialized <a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdoutboundattachment">IWSDOutboundAttachment</a> object. Cannot be <b>NULL</b>.

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
<i>attachmentOut</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>