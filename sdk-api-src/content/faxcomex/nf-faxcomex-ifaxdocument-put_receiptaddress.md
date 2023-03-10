---
UID: NF:faxcomex.IFaxDocument.put_ReceiptAddress
title: IFaxDocument::put_ReceiptAddress (faxcomex.h)
description: The IFaxDocument::get_ReceiptAddress property is a null-terminated string that indicates the email address to which the fax service should send a delivery receipt when the fax job reaches a final state. (Put)
helpviewer_keywords: ["IFaxDocument interface [Fax Service]","ReceiptAddress property","IFaxDocument.ReceiptAddress","IFaxDocument.get_ReceiptAddress","IFaxDocument.put_ReceiptAddress","IFaxDocument::ReceiptAddress","IFaxDocument::get_ReceiptAddress","IFaxDocument::put_ReceiptAddress","ReceiptAddress property [Fax Service]","ReceiptAddress property [Fax Service]","IFaxDocument interface","_mfax_faxdocument.receiptaddress","fax._mfax_faxdocument_cpp_mfax_faxdocument_receiptaddress_cpp","fax._mfax_faxdocument_receiptaddress","faxcomex/IFaxDocument::ReceiptAddress","faxcomex/IFaxDocument::get_ReceiptAddress","faxcomex/IFaxDocument::put_ReceiptAddress","put_ReceiptAddress"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_receiptaddress_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9y9f.htm
ms.date: 12/05/2018
ms.keywords: IFaxDocument interface [Fax Service],ReceiptAddress property, IFaxDocument.ReceiptAddress, IFaxDocument.get_ReceiptAddress, IFaxDocument.put_ReceiptAddress, IFaxDocument::ReceiptAddress, IFaxDocument::get_ReceiptAddress, IFaxDocument::put_ReceiptAddress, ReceiptAddress property [Fax Service], ReceiptAddress property [Fax Service],IFaxDocument interface, _mfax_faxdocument.receiptaddress, fax._mfax_faxdocument_cpp_mfax_faxdocument_receiptaddress_cpp, fax._mfax_faxdocument_receiptaddress, faxcomex/IFaxDocument::ReceiptAddress, faxcomex/IFaxDocument::get_ReceiptAddress, faxcomex/IFaxDocument::put_ReceiptAddress, put_ReceiptAddress
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
 - IFaxDocument::put_ReceiptAddress
 - faxcomex/IFaxDocument::put_ReceiptAddress
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
 - IFaxDocument.ReceiptAddress
 - IFaxDocument.get_ReceiptAddress
 - IFaxDocument.put_ReceiptAddress
 - IFaxDocument.get_ReceiptAddress
 - IFaxDocument.put_ReceiptAddress
---

# IFaxDocument::put_ReceiptAddress


## -description

The <b>IFaxDocument::get_ReceiptAddress</b> property is a null-terminated string that indicates the email address to which the fax service should send a delivery receipt when the fax job reaches a final state.

This property is read/write.

## -parameters

## -remarks

This property has meaning only if the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-receipttype-vb">ReceiptType</a> property for the document is set to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_receipt_type_enum">frtMail</a>, indicating that the delivery receipt will be sent by email.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
