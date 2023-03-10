---
UID: NF:faxcomex.IFaxDocument.put_AttachFaxToReceipt
title: IFaxDocument::put_AttachFaxToReceipt (faxcomex.h)
description: The IFaxDocument::get_AttachFaxToReceipt property indicates whether to attach a fax to the receipt. (Put)
helpviewer_keywords: ["AttachFaxToReceipt property [Fax Service]","AttachFaxToReceipt property [Fax Service]","IFaxDocument interface","IFaxDocument interface [Fax Service]","AttachFaxToReceipt property","IFaxDocument.AttachFaxToReceipt","IFaxDocument.put_AttachFaxToReceipt","IFaxDocument::AttachFaxToReceipt","IFaxDocument::get_AttachFaxToReceipt","IFaxDocument::put_AttachFaxToReceipt","_mfax_faxdocument.attachfaxtoreceipt","fax._mfax_faxdocument_attachfaxtoreceipt","fax._mfax_faxdocument_cpp_mfax_faxdocument_attachfaxtoreceipt_cpp","faxcomex/IFaxDocument::AttachFaxToReceipt","faxcomex/IFaxDocument::get_AttachFaxToReceipt","faxcomex/IFaxDocument::put_AttachFaxToReceipt","put_AttachFaxToReceipt"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_attachfaxtoreceipt_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5blg.htm
ms.date: 12/05/2018
ms.keywords: AttachFaxToReceipt property [Fax Service], AttachFaxToReceipt property [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],AttachFaxToReceipt property, IFaxDocument.AttachFaxToReceipt, IFaxDocument.put_AttachFaxToReceipt, IFaxDocument::AttachFaxToReceipt, IFaxDocument::get_AttachFaxToReceipt, IFaxDocument::put_AttachFaxToReceipt, _mfax_faxdocument.attachfaxtoreceipt, fax._mfax_faxdocument_attachfaxtoreceipt, fax._mfax_faxdocument_cpp_mfax_faxdocument_attachfaxtoreceipt_cpp, faxcomex/IFaxDocument::AttachFaxToReceipt, faxcomex/IFaxDocument::get_AttachFaxToReceipt, faxcomex/IFaxDocument::put_AttachFaxToReceipt, put_AttachFaxToReceipt
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
 - IFaxDocument::put_AttachFaxToReceipt
 - faxcomex/IFaxDocument::put_AttachFaxToReceipt
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
 - IFaxDocument.AttachFaxToReceipt
 - IFaxDocument.get_AttachFaxToReceipt
 - IFaxDocument.put_AttachFaxToReceipt
---

# IFaxDocument::put_AttachFaxToReceipt


## -description

The <b>IFaxDocument::get_AttachFaxToReceipt</b> property indicates whether to attach a fax to the receipt.

This property is read/write.

## -parameters

## -remarks

By default, <b>IFaxDocument::get_AttachFaxToReceipt</b> is set to <b>FALSE</b>.

When a fax consisting only of a cover page is sent to multiple recipients, you cannot attach the fax to the receipt because the fax differs for each recipient. If there is a fax body, then the body can be attached to the receipt, even when there are multiple recipients.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
