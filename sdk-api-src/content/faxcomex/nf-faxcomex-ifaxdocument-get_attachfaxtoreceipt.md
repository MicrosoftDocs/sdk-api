---
UID: NF:faxcomex.IFaxDocument.get_AttachFaxToReceipt
title: IFaxDocument::get_AttachFaxToReceipt
author: windows-sdk-content
description: The IFaxDocument::get_AttachFaxToReceipt property indicates whether to attach a fax to the receipt.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_attachfaxtoreceipt_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5blg.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: AttachFaxToReceipt property [Fax Service], AttachFaxToReceipt property [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],AttachFaxToReceipt property, IFaxDocument.AttachFaxToReceipt, IFaxDocument.get_AttachFaxToReceipt, IFaxDocument::AttachFaxToReceipt, IFaxDocument::get_AttachFaxToReceipt, IFaxDocument::put_AttachFaxToReceipt, _mfax_faxdocument.attachfaxtoreceipt, fax._mfax_faxdocument_attachfaxtoreceipt, fax._mfax_faxdocument_cpp_mfax_faxdocument_attachfaxtoreceipt_cpp, faxcomex/IFaxDocument::AttachFaxToReceipt, faxcomex/IFaxDocument::get_AttachFaxToReceipt, faxcomex/IFaxDocument::put_AttachFaxToReceipt, get_AttachFaxToReceipt
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
 - IFaxDocument.AttachFaxToReceipt
 - IFaxDocument.get_AttachFaxToReceipt
 - IFaxDocument.put_AttachFaxToReceipt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::get_AttachFaxToReceipt


## -description


The <b>IFaxDocument::get_AttachFaxToReceipt</b> property indicates whether to attach a fax to the receipt.

This property is read/write.


## -parameters


## -remarks



By default, <b>IFaxDocument::get_AttachFaxToReceipt</b> is set to <b>FALSE</b>.

When a fax consisting only of a cover page is sent to multiple recipients, you cannot attach the fax to the receipt because the fax differs for each recipient. If there is a fax body, then the body can be attached to the receipt, even when there are multiple recipients.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

