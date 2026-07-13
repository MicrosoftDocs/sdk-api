---
UID: NF:faxcomex.IFaxDocument.put_ReceiptType
title: IFaxDocument::put_ReceiptType (faxcomex.h)
description: The IFaxDocument::get_ReceiptType property specifies the type of delivery receipt to deliver when the fax job reaches a final state. (Put)
helpviewer_keywords: ["IFaxDocument interface [Fax Service]","ReceiptType property","IFaxDocument.ReceiptType","IFaxDocument.get_ReceiptType","IFaxDocument.put_ReceiptType","IFaxDocument::ReceiptType","IFaxDocument::get_ReceiptType","IFaxDocument::put_ReceiptType","ReceiptType property [Fax Service]","ReceiptType property [Fax Service]","IFaxDocument interface","_mfax_faxdocument.receipttype","fax._mfax_faxdocument_cpp_mfax_faxdocument_receipttype_cpp","fax._mfax_faxdocument_receipttype","faxcomex/IFaxDocument::ReceiptType","faxcomex/IFaxDocument::get_ReceiptType","faxcomex/IFaxDocument::put_ReceiptType","put_ReceiptType"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_receipttype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_75ut.htm
ms.date: 12/05/2018
ms.keywords: IFaxDocument interface [Fax Service],ReceiptType property, IFaxDocument.ReceiptType, IFaxDocument.get_ReceiptType, IFaxDocument.put_ReceiptType, IFaxDocument::ReceiptType, IFaxDocument::get_ReceiptType, IFaxDocument::put_ReceiptType, ReceiptType property [Fax Service], ReceiptType property [Fax Service],IFaxDocument interface, _mfax_faxdocument.receipttype, fax._mfax_faxdocument_cpp_mfax_faxdocument_receipttype_cpp, fax._mfax_faxdocument_receipttype, faxcomex/IFaxDocument::ReceiptType, faxcomex/IFaxDocument::get_ReceiptType, faxcomex/IFaxDocument::put_ReceiptType, put_ReceiptType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDocument::put_ReceiptType
 - faxcomex/IFaxDocument::put_ReceiptType
dev_langs:
 - c++
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
---

# IFaxDocument::put_ReceiptType


## -description

The <b>IFaxDocument::get_ReceiptType</b> property specifies the type of delivery receipt to deliver when the fax job reaches a final state.

This property is read/write.

## -parameters

## -remarks

The fax service sends a report (a delivery receipt) to the sender of the fax when the fax completes successfully or when the fax transmission fails.

If an email receipt will be sent, an address has to be provided in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-receiptaddress-vb">IFaxDocument::get_ReceiptAddress</a> property. If the receipt type is set to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_receipt_type_enum">frtMSGBOX</a>, the message box will appear on the computer from which the document was sent. By default, <b>ReceiptType</b> is set to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_receipt_type_enum">frtNONE</a>, indicating that no receipt will be sent.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
