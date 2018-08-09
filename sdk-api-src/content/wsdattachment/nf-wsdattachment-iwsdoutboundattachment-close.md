---
UID: NF:wsdattachment.IWSDOutboundAttachment.Close
title: IWSDOutboundAttachment::Close
author: windows-sdk-content
description: Closes the current attachment MIME data stream.
old-location: ncd\iwsdoutboundattachment_close_method.htm
old-project: wsdapi
ms.assetid: 8ab63ed5-7b71-4f28-926d-a24666f0dd15
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Close, Close method, Close method,IWSDOutboundAttachment interface, IWSDOutboundAttachment interface,Close method, IWSDOutboundAttachment.Close, IWSDOutboundAttachment::Close, ncd.iwsdoutboundattachment_close_method, wsdattachment/IWSDOutboundAttachment::Close
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WSC_SECURITY_PROVIDER_HEALTH, *PWSC_SECURITY_PROVIDER_HEALTH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDOutboundAttachment.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDOutboundAttachment::Close


## -description


Closes the current attachment MIME data stream.


## -parameters






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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> was called before <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> was called. You must call <b>Write</b> before closing the attachment stream.

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

<b>Close</b> may block while waiting for a previous <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> operation to complete.
<b>Close</b> may block for up to 30 seconds (per HTTP transmission timeouts) while waiting for a  previous <b>Write</b> operation to complete.


 The <b>Close</b> method may return successfully after a failed  <b>Close</b> attempt that returned <b>STG_S_BLOCK</b>.  A subsequent success indicates that the internal buffers were freed for use after the initial failed attempt. When <b>STG_S_BLOCK</b> is received by an application, the application can either call <b>Close</b> again or terminate  the data transfer using the <a href="https://msdn.microsoft.com/add0160c-bbf7-446e-8592-a05fd4d16fac">Abort</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1bacbf20-2eb2-4aa1-ba37-e14dc0d955b0">IWSDInboundAttachment</a>



<a href="https://msdn.microsoft.com/ba2f2038-e6ef-4ad4-a1fb-50e225394c60">IWSDOutboundAttachment</a>



<a href="https://msdn.microsoft.com/add0160c-bbf7-446e-8592-a05fd4d16fac">IWSDOutboundAttachment::Abort</a>



<a href="https://msdn.microsoft.com/5bd24e7c-f2f4-4cc4-abc0-176ed024fa43">IWSDOutboundAttachment::Write</a>
 

 

