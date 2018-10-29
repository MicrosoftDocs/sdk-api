---
UID: NF:faxcomex.IFaxDocument.get_ReceiptAddress
title: IFaxDocument::get_ReceiptAddress
author: windows-sdk-content
description: The IFaxDocument::get_ReceiptAddress property is a null-terminated string that indicates the email address to which the fax service should send a delivery receipt when the fax job reaches a final state.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_receiptaddress_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9y9f.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxDocument interface [Fax Service],ReceiptAddress property, IFaxDocument.ReceiptAddress, IFaxDocument.get_ReceiptAddress, IFaxDocument.put_ReceiptAddress, IFaxDocument::ReceiptAddress, IFaxDocument::get_ReceiptAddress, IFaxDocument::put_ReceiptAddress, ReceiptAddress property [Fax Service], ReceiptAddress property [Fax Service],IFaxDocument interface, _mfax_faxdocument.receiptaddress, fax._mfax_faxdocument_cpp_mfax_faxdocument_receiptaddress_cpp, fax._mfax_faxdocument_receiptaddress, faxcomex/IFaxDocument::ReceiptAddress, faxcomex/IFaxDocument::get_ReceiptAddress, faxcomex/IFaxDocument::put_ReceiptAddress, get_ReceiptAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDocument.ReceiptAddress
 - IFaxDocument.get_ReceiptAddress
 - IFaxDocument.put_ReceiptAddress
 - IFaxDocument.get_ReceiptAddress
 - IFaxDocument.put_ReceiptAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::get_ReceiptAddress


## -description


The <b>IFaxDocument::get_ReceiptAddress</b> property is a null-terminated string that indicates the email address to which the fax service should send a delivery receipt when the fax job reaches a final state.

This property is read/write.


## -parameters


## -remarks



This property has meaning only if the <a href="https://msdn.microsoft.com/ee8f9070-7f00-4bd4-8022-1d9b00f1bdaa">ReceiptType</a> property for the document is set to <a href="https://msdn.microsoft.com/d334b8e4-bc4f-4f1f-9268-65a2106d3fa6">frtMail</a>, indicating that the delivery receipt will be sent by email.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

