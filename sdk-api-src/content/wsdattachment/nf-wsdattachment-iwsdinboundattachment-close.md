---
UID: NF:wsdattachment.IWSDInboundAttachment.Close
title: IWSDInboundAttachment::Close (wsdattachment.h)
description: Closes the current attachment MIME data stream. (IWSDInboundAttachment.Close)
helpviewer_keywords: ["Close","Close method","Close method","IWSDInboundAttachment interface","IWSDInboundAttachment interface","Close method","IWSDInboundAttachment.Close","IWSDInboundAttachment::Close","ncd.iwsdinboundattachment_close","wsdattachment/IWSDInboundAttachment::Close"]
old-location: ncd\iwsdinboundattachment_close.htm
tech.root: ncd
ms.assetid: 1bd0295c-4c37-42ec-b5a5-dc7f467def05
ms.date: 12/05/2018
ms.keywords: Close, Close method, Close method,IWSDInboundAttachment interface, IWSDInboundAttachment interface,Close method, IWSDInboundAttachment.Close, IWSDInboundAttachment::Close, ncd.iwsdinboundattachment_close, wsdattachment/IWSDInboundAttachment::Close
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
 - IWSDInboundAttachment::Close
 - wsdattachment/IWSDInboundAttachment::Close
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
 - IWSDInboundAttachment.Close
---

# IWSDInboundAttachment::Close


## -description

Closes the current attachment MIME data stream.



## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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

This method can be used to terminate the transfer of an incoming attachment while the transfer is in progress. 

Usually, <b>Close</b> must be called before calling <b>Release()</b> on the <a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdinboundattachment">IWSDInboundAttachment</a>  interface. The only time a <b>Close</b> call is not required is when <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdinboundattachment-read">Read</a> returns S_FALSE, which indicates that the end of the attachment stream has been reached. In that case, simply call  <b>Release()</b> on the <b>IWSDInboundAttachment</b>  interface.

## -see-also

<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdinboundattachment">IWSDInboundAttachment</a>
