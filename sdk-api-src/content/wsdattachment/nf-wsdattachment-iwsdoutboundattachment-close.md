---
UID: NF:wsdattachment.IWSDOutboundAttachment.Close
title: IWSDOutboundAttachment::Close (wsdattachment.h)
description: Closes the current attachment MIME data stream. (IWSDOutboundAttachment.Close)
helpviewer_keywords: ["Close","Close method","Close method","IWSDOutboundAttachment interface","IWSDOutboundAttachment interface","Close method","IWSDOutboundAttachment.Close","IWSDOutboundAttachment::Close","ncd.iwsdoutboundattachment_close_method","wsdattachment/IWSDOutboundAttachment::Close"]
old-location: ncd\iwsdoutboundattachment_close_method.htm
tech.root: ncd
ms.assetid: 8ab63ed5-7b71-4f28-926d-a24666f0dd15
ms.date: 12/05/2018
ms.keywords: Close, Close method, Close method,IWSDOutboundAttachment interface, IWSDOutboundAttachment interface,Close method, IWSDOutboundAttachment.Close, IWSDOutboundAttachment::Close, ncd.iwsdoutboundattachment_close_method, wsdattachment/IWSDOutboundAttachment::Close
req.header: wsdattachment.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdAttachment.idl
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
 - IWSDOutboundAttachment::Close
 - wsdattachment/IWSDOutboundAttachment::Close
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
 - IWSDOutboundAttachment.Close
---

# IWSDOutboundAttachment::Close


## -description

Closes the current attachment MIME data stream.



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
Method completed successfully. All data in the attachment stream was successfully transferred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">Close</a> was called before <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">Write</a> was called. You must call <b>Write</b> before closing the attachment stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_S_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
Internal buffers were not available. The data in the attachment stream was not successfully transferred.

</td>
</tr>
</table>

## -remarks

<b>Close</b> is used to indicate that the application has no more data to transmit in the current attachment stream. The return value can indicate an error in a previous Write operation or an issue closing the connection.

<b>Close</b> may block while waiting for a previous <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">Write</a> operation to complete.
<b>Close</b> may block for up to 30 seconds (per HTTP transmission timeouts) while waiting for a  previous <b>Write</b> operation to complete.


 The <b>Close</b> method may return successfully after a failed  <b>Close</b> attempt that returned <b>STG_S_BLOCK</b>.  A subsequent success indicates that the internal buffers were freed for use after the initial failed attempt. When <b>STG_S_BLOCK</b> is received by an application, the application can either call <b>Close</b> again or terminate  the data transfer using the <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-abort">Abort</a> method.

## -see-also

<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdinboundattachment">IWSDInboundAttachment</a>



<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdoutboundattachment">IWSDOutboundAttachment</a>



<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-abort">IWSDOutboundAttachment::Abort</a>



<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">IWSDOutboundAttachment::Write</a>
