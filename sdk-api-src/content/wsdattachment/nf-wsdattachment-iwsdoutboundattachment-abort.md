---
UID: NF:wsdattachment.IWSDOutboundAttachment.Abort
title: IWSDOutboundAttachment::Abort (wsdattachment.h)
description: Aborts the transfer of data on the attachment MIME data stream.
helpviewer_keywords: ["Abort","Abort method","Abort method","IWSDOutboundAttachment interface","IWSDOutboundAttachment interface","Abort method","IWSDOutboundAttachment.Abort","IWSDOutboundAttachment::Abort","ncd.iwsdoutboundattachment_abort","wsdattachment/IWSDOutboundAttachment::Abort"]
old-location: ncd\iwsdoutboundattachment_abort.htm
tech.root: ncd
ms.assetid: add0160c-bbf7-446e-8592-a05fd4d16fac
ms.date: 12/05/2018
ms.keywords: Abort, Abort method, Abort method,IWSDOutboundAttachment interface, IWSDOutboundAttachment interface,Abort method, IWSDOutboundAttachment.Abort, IWSDOutboundAttachment::Abort, ncd.iwsdoutboundattachment_abort, wsdattachment/IWSDOutboundAttachment::Abort
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
 - IWSDOutboundAttachment::Abort
 - wsdattachment/IWSDOutboundAttachment::Abort
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
 - IWSDOutboundAttachment.Abort
---

# IWSDOutboundAttachment::Abort


## -description

Aborts the transfer of data on the attachment MIME data stream. When <b>Abort</b> is called, any pending data may be discarded.



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
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-abort">Abort</a> was called before <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">Write</a> was called. You must call <b>Write</b> before terminating the attachment stream.

</td>
</tr>
</table>

## -remarks

The <b>Abort</b> method may be called when a <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">Close</a> or <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">Write</a> method call failed with the error <b>STG_S_BLOCK</b>.


<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">Close</a> must not be called once <b>Abort</b> has been called on an attachment stream.

## -see-also

<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdoutboundattachment">IWSDOutboundAttachment</a>



<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">IWSDOutboundAttachment::Close</a>



<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">IWSDOutboundAttachment::Write</a>
