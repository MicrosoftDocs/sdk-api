---
UID: NF:faxcomex.IFaxOutgoingJob2.get_ReceiptAddress
title: IFaxOutgoingJob2::get_ReceiptAddress (faxcomex.h)
description: A null-terminated string containing the address to which a delivery report will be sent, indicating success or failure.
helpviewer_keywords: ["IFaxOutgoingJob2 interface [Fax Service]","ReceiptAddress property","IFaxOutgoingJob2.ReceiptAddress","IFaxOutgoingJob2.get_ReceiptAddress","IFaxOutgoingJob2::ReceiptAddress","IFaxOutgoingJob2::get_ReceiptAddress","ReceiptAddress property [Fax Service]","ReceiptAddress property [Fax Service]","IFaxOutgoingJob2 interface","_mfax_faxoutgoingjob.receiptaddress","fax._mfax_faxoutgoingjob2_cpp_mfax_faxoutgoingjob_receiptaddress_cpp","fax._mfax_faxoutgoingjob_receiptaddress","faxcomex/IFaxOutgoingJob2::ReceiptAddress","faxcomex/IFaxOutgoingJob2::get_ReceiptAddress","get_ReceiptAddress"]
old-location: fax\_mfax_faxoutgoingjob2_cpp_mfax_faxoutgoingjob_receiptaddress_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingjob2\receiptaddress.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob2 interface [Fax Service],ReceiptAddress property, IFaxOutgoingJob2.ReceiptAddress, IFaxOutgoingJob2.get_ReceiptAddress, IFaxOutgoingJob2::ReceiptAddress, IFaxOutgoingJob2::get_ReceiptAddress, ReceiptAddress property [Fax Service], ReceiptAddress property [Fax Service],IFaxOutgoingJob2 interface, _mfax_faxoutgoingjob.receiptaddress, fax._mfax_faxoutgoingjob2_cpp_mfax_faxoutgoingjob_receiptaddress_cpp, fax._mfax_faxoutgoingjob_receiptaddress, faxcomex/IFaxOutgoingJob2::ReceiptAddress, faxcomex/IFaxOutgoingJob2::get_ReceiptAddress, get_ReceiptAddress
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxOutgoingJob2::get_ReceiptAddress
 - faxcomex/IFaxOutgoingJob2::get_ReceiptAddress
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
 - IFaxOutgoingJob2.ReceiptAddress
 - IFaxOutgoingJob2.get_ReceiptAddress
 - IFaxOutgoingJob2.get_ReceiptAddress
---

# IFaxOutgoingJob2::get_ReceiptAddress


## -description

A null-terminated string containing the address to which a delivery report will be sent, indicating success or failure. 

This property is read-only.

## -parameters

## -remarks

The type of address will vary according to the value of the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-receipttype-vb">ReceiptType</a> property as indicated in this table.

<table class="clsStd">
<tr>
<th>Value of <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-receipttype-vb">ReceiptType</a> property</th>
<th>Type of address</th>
</tr>
<tr>
<td>frtMAIL</td>
<td>An SMTP email address</td>
</tr>
<tr>
<td>frtMSGBOX</td>
<td>The computer name on which the delivery report message box will appear</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob2">IFaxOutgoingJob2</a>