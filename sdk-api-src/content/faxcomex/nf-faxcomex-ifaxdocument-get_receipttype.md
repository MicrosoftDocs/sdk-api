---
UID: NF:faxcomex.IFaxDocument.get_ReceiptType
title: IFaxDocument::get_ReceiptType
author: windows-sdk-content
description: The IFaxDocument::get_ReceiptType property specifies the type of delivery receipt to deliver when the fax job reaches a final state.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_receipttype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_75ut.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxDocument interface [Fax Service],ReceiptType property, IFaxDocument.ReceiptType, IFaxDocument.get_ReceiptType, IFaxDocument.put_ReceiptType, IFaxDocument::ReceiptType, IFaxDocument::get_ReceiptType, IFaxDocument::put_ReceiptType, ReceiptType property [Fax Service], ReceiptType property [Fax Service],IFaxDocument interface, _mfax_faxdocument.receipttype, fax._mfax_faxdocument_cpp_mfax_faxdocument_receipttype_cpp, fax._mfax_faxdocument_receipttype, faxcomex/IFaxDocument::ReceiptType, faxcomex/IFaxDocument::get_ReceiptType, faxcomex/IFaxDocument::put_ReceiptType, get_ReceiptType
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
 - IFaxDocument.ReceiptType
 - IFaxDocument.get_ReceiptType
 - IFaxDocument.put_ReceiptType
 - IFaxDocument.get_ReceiptType
 - IFaxDocument.put_ReceiptType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::get_ReceiptType


## -description


The <b>IFaxDocument::get_ReceiptType</b> property specifies the type of delivery receipt to deliver when the fax job reaches a final state.

This property is read/write.


## -parameters


## -remarks



The fax service sends a report (a delivery receipt) to the sender of the fax when the fax completes successfully or when the fax transmission fails.

If an email receipt will be sent, an address has to be provided in the <a href="https://msdn.microsoft.com/aa704480-0db8-4b06-9443-74b4d5981fd8">IFaxDocument::get_ReceiptAddress</a> property. If the receipt type is set to <a href="https://msdn.microsoft.com/d334b8e4-bc4f-4f1f-9268-65a2106d3fa6">frtMSGBOX</a>, the message box will appear on the computer from which the document was sent. By default, <b>ReceiptType</b> is set to <a href="https://msdn.microsoft.com/d334b8e4-bc4f-4f1f-9268-65a2106d3fa6">frtNONE</a>, indicating that no receipt will be sent.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

