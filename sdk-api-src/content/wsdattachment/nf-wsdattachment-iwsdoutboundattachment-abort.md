---
UID: NF:wsdattachment.IWSDOutboundAttachment.Abort
title: IWSDOutboundAttachment::Abort
author: windows-sdk-content
description: Aborts the transfer of data on the attachment MIME data stream.
old-location: ncd\iwsdoutboundattachment_abort.htm
tech.root: wsdapi
ms.assetid: add0160c-bbf7-446e-8592-a05fd4d16fac
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Abort, Abort method, Abort method,IWSDOutboundAttachment interface, IWSDOutboundAttachment interface,Abort method, IWSDOutboundAttachment.Abort, IWSDOutboundAttachment::Abort, ncd.iwsdoutboundattachment_abort, wsdattachment/IWSDOutboundAttachment::Abort
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDOutboundAttachment.Abort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDOutboundAttachment::Abort


## -description


Aborts the transfer of data on the attachment MIME data stream. When <b>Abort</b> is called, any pending data may be discarded.


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

<a href="https://msdn.microsoft.com/add0160c-bbf7-446e-8592-a05fd4d16fac">Abort</a> was called before <a href="https://msdn.microsoft.com/5bd24e7c-f2f4-4cc4-abc0-176ed024fa43">Write</a> was called. You must call <b>Write</b> before terminating the attachment stream.

</td>
</tr>
</table>
 




## -remarks



The <b>Abort</b> method may be called when a <a href="https://msdn.microsoft.com/8ab63ed5-7b71-4f28-926d-a24666f0dd15">Close</a> or <a href="https://msdn.microsoft.com/5bd24e7c-f2f4-4cc4-abc0-176ed024fa43">Write</a> method call failed with the error <b>STG_S_BLOCK</b>.


<a href="https://msdn.microsoft.com/8ab63ed5-7b71-4f28-926d-a24666f0dd15">Close</a> must not be called once <b>Abort</b> has been called on an attachment stream.




## -see-also




<a href="https://msdn.microsoft.com/ba2f2038-e6ef-4ad4-a1fb-50e225394c60">IWSDOutboundAttachment</a>



<a href="https://msdn.microsoft.com/8ab63ed5-7b71-4f28-926d-a24666f0dd15">IWSDOutboundAttachment::Close</a>



<a href="https://msdn.microsoft.com/5bd24e7c-f2f4-4cc4-abc0-176ed024fa43">IWSDOutboundAttachment::Write</a>
 

 

