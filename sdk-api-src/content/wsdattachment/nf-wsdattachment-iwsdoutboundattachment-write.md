---
UID: NF:wsdattachment.IWSDOutboundAttachment.Write
title: IWSDOutboundAttachment::Write (wsdattachment.h)
description: Sends attachment data to the remote host using a MIME container.
helpviewer_keywords: ["IWSDOutboundAttachment interface","Write method","IWSDOutboundAttachment.Write","IWSDOutboundAttachment::Write","Write","Write method","Write method","IWSDOutboundAttachment interface","ncd.iwsdoutboundattachment_write_method","wsdattachment/IWSDOutboundAttachment::Write"]
old-location: ncd\iwsdoutboundattachment_write_method.htm
tech.root: ncd
ms.assetid: 5bd24e7c-f2f4-4cc4-abc0-176ed024fa43
ms.date: 12/05/2018
ms.keywords: IWSDOutboundAttachment interface,Write method, IWSDOutboundAttachment.Write, IWSDOutboundAttachment::Write, Write, Write method, Write method,IWSDOutboundAttachment interface, ncd.iwsdoutboundattachment_write_method, wsdattachment/IWSDOutboundAttachment::Write
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
 - IWSDOutboundAttachment::Write
 - wsdattachment/IWSDOutboundAttachment::Write
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
 - IWSDOutboundAttachment.Write
---

# IWSDOutboundAttachment::Write


## -description

Sends attachment data to the remote host using a MIME container.

## -parameters

### -param pBuffer [in]

Pointer to a buffer containing the output data. The application program is responsible for allocating and freeing this data buffer.

### -param dwBytesToWrite [in]

Number of bytes to send to the remote host from <i>pBuffer</i>.

### -param pdwNumberOfBytesWritten [out]

Pointer to a <b>DWORD</b> containing the number of bytes of data actually sent to the remote host.

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
<i>pdwNumberofBytesWritten</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pBuffer</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
The outbound attachment interface has not been initialized. Call <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-wsdcreateoutboundattachment">WSDCreateOutboundAttachment</a> to initialize the interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_S_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
Internal buffers were not available. The data was not accepted and queued for transmission.

</td>
</tr>
</table>

## -remarks

The <b>Write</b> method allows an application program to send arbitrary data to a remote host as a MIME-encapsulated message attachment. The first call to  <b>Write</b> opens the outbound attachment stream and initiates transmission of the HTTP headers, envelope data, and the MIME-encoded application data. Subsequent calls to <b>Write</b> will send additional blocks of MIME-encoded application data until the application makes a call to <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">Close</a>, which closes the attachment stream and finishes the transmission of the message envelope data and headers.

 The <b>Write</b> operation may block under several conditions. On the initial operation, <b>Write</b> will block until the HTTP headers and XML content have been transmitted. When sending multiple attachments in a single message, the first call to <b>Write</b> on any attachment may block until any prior attachment streams have been completely transmitted.
<b>Write</b> may block for up to 30 seconds (per HTTP transmission timeouts) if the remote host does not reply.

If an error occurs in establishing a connection or transmitting headers, <b>Write</b> will return the error code immediately. If a data transfer error occurs, the error may be delayed to a future call of <b>Write</b> or <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">Close</a>.

 The <b>Write</b> method may return successfully after a failed  <b>Write</b> attempt that returned <b>STG_S_BLOCK</b>.  A subsequent success indicates that the internal buffers were freed for use after the initial failed attempt. When <b>STG_S_BLOCK</b> is received by an application, the application can either resend the same data using the <b>Write</b> method or terminate  the data transfer using the <a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-abort">Abort</a> method.

## -see-also

<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdinboundattachment">IWSDInboundAttachment</a>



<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdoutboundattachment">IWSDOutboundAttachment</a>



<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-abort">IWSDOutboundAttachment::Abort</a>



<a href="/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">IWSDOutboundAttachment::Close</a>