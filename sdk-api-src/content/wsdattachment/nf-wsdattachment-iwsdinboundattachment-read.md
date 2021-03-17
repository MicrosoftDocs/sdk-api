---
UID: NF:wsdattachment.IWSDInboundAttachment.Read
title: IWSDInboundAttachment::Read (wsdattachment.h)
description: Retrieves attachment data from a message sent by a remote host.
helpviewer_keywords: ["IWSDInboundAttachment interface","Read method","IWSDInboundAttachment.Read","IWSDInboundAttachment::Read","Read","Read method","Read method","IWSDInboundAttachment interface","ncd.iwsdinboundattachment_read_method","wsdattachment/IWSDInboundAttachment::Read"]
old-location: ncd\iwsdinboundattachment_read_method.htm
tech.root: ncd
ms.assetid: 66b8ce84-23b3-43f2-826d-c866b8bedab1
ms.date: 12/05/2018
ms.keywords: IWSDInboundAttachment interface,Read method, IWSDInboundAttachment.Read, IWSDInboundAttachment::Read, Read, Read method, Read method,IWSDInboundAttachment interface, ncd.iwsdinboundattachment_read_method, wsdattachment/IWSDInboundAttachment::Read
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
 - IWSDInboundAttachment::Read
 - wsdattachment/IWSDInboundAttachment::Read
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
 - IWSDInboundAttachment.Read
---

# IWSDInboundAttachment::Read


## -description

Retrieves attachment data from a message sent by a remote host.

## -parameters

### -param pBuffer [out]

Pointer to a buffer receiving the data read from the attachment stream. The application program is responsible for allocating and freeing this data buffer.

### -param dwBytesToRead [in]

Size of the <i>pBuffer</i> input buffer, in bytes.

### -param pdwNumberOfBytesRead [out]

Pointer to a <b>DWORD</b> containing the number of bytes of data read from the attachment stream into the <i>pBuffer</i> input buffer.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The end of the attachment stream has been reached.  

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwNumberofBytesRead</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>Read</b> method allows an application to receive arbitrary data from a remote host in a MIME-encapsulated message attachment. WSDAPI will provide an object implementing this interface when an attachment stream is received as part of a message. The call to <b>Read</b> opens the inbound attachment stream and transfers the attachment data to the application's buffer. If <b>Read</b> returns S_OK or S_FALSE, <i>pdwNumberofBytesRead</i> is set to the number of bytes read, which may be less than the size of the buffer. The <b>Read</b> call may block on network traffic.

## -see-also

<a href="/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdinboundattachment">IWSDInboundAttachment</a>