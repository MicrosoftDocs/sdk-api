---
UID: NF:faxcomex.IFaxOutgoingMessage2.get_ReceiptAddress
title: IFaxOutgoingMessage2::get_ReceiptAddress (faxcomex.h)
description: Specifies the address to which the delivery report is sent.
helpviewer_keywords: ["IFaxOutgoingMessage2 interface [Fax Service]","ReceiptAddress property","IFaxOutgoingMessage2.ReceiptAddress","IFaxOutgoingMessage2.get_ReceiptAddress","IFaxOutgoingMessage2::ReceiptAddress","IFaxOutgoingMessage2::get_ReceiptAddress","ReceiptAddress property [Fax Service]","ReceiptAddress property [Fax Service]","IFaxOutgoingMessage2 interface","_mfax_faxoutgoingmessage.receiptaddress","fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_receiptaddress_cpp","fax._mfax_faxoutgoingmessage_receiptaddress","faxcomex/IFaxOutgoingMessage2::ReceiptAddress","faxcomex/IFaxOutgoingMessage2::get_ReceiptAddress","get_ReceiptAddress"]
old-location: fax\_mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_receiptaddress_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\receiptaddress.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessage2 interface [Fax Service],ReceiptAddress property, IFaxOutgoingMessage2.ReceiptAddress, IFaxOutgoingMessage2.get_ReceiptAddress, IFaxOutgoingMessage2::ReceiptAddress, IFaxOutgoingMessage2::get_ReceiptAddress, ReceiptAddress property [Fax Service], ReceiptAddress property [Fax Service],IFaxOutgoingMessage2 interface, _mfax_faxoutgoingmessage.receiptaddress, fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_receiptaddress_cpp, fax._mfax_faxoutgoingmessage_receiptaddress, faxcomex/IFaxOutgoingMessage2::ReceiptAddress, faxcomex/IFaxOutgoingMessage2::get_ReceiptAddress, get_ReceiptAddress
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
 - IFaxOutgoingMessage2::get_ReceiptAddress
 - faxcomex/IFaxOutgoingMessage2::get_ReceiptAddress
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
 - IFaxOutgoingMessage2.ReceiptAddress
 - IFaxOutgoingMessage2.get_ReceiptAddress
 - IFaxOutgoingMessage2.get_ReceiptAddress
---

# IFaxOutgoingMessage2::get_ReceiptAddress


## -description

Specifies the address to which the delivery report is sent. 


<div class="alert"><b>Note</b>  This property is supported only on Windows Vista and later.</div><div> </div>This property is read-only.

## -parameters

## -remarks

The type of address will vary according to the value of the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-receipttype-vb">IFaxOutgoingMessage2::ReceiptType</a> property as indicated in this table.

<table class="clsStd">
<tr>
<th>Value of <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-receipttype-vb">IFaxOutgoingMessage2::ReceiptType</a> property</th>
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

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage2">IFaxOutgoingMessage2</a>