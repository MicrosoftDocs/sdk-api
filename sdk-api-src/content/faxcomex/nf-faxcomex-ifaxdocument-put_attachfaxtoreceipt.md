---
UID: NF:faxcomex.IFaxDocument.put_AttachFaxToReceipt
title: IFaxDocument::put_AttachFaxToReceipt
author: windows-sdk-content
description: The AttachFaxToReceipt property indicates whether to attach a fax to the receipt.
old-location: fax\_mfax_faxdocument_attachfaxtoreceipt_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5blg.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: AttachFaxToReceipt property [Fax Service], AttachFaxToReceipt property [Fax Service],FaxDocument object, FaxDocument object [Fax Service],AttachFaxToReceipt property, FaxDocument.AttachFaxToReceipt, IFaxDocument.put_AttachFaxToReceipt, IFaxDocument::put_AttachFaxToReceipt, _mfax_faxdocument.attachfaxtoreceipt, fax._mfax_faxdocument_attachfaxtoreceipt, fax._mfax_faxdocument_attachfaxtoreceipt_vb, put_AttachFaxToReceipt
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxDocument.AttachFaxToReceipt
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument::put_AttachFaxToReceipt


## -description


The <b>AttachFaxToReceipt</b> property indicates whether to attach a fax to the receipt.

This property is read/write.


## -parameters


## -remarks



By default, <b>AttachFaxToReceipt</b> is set to <b>False</b>.

When a fax consisting only of a cover page is sent to multiple recipients, you cannot attach the fax to the receipt because the fax differs for each recipient. If there is a fax body, then the body can be attached to the receipt, even when there are multiple recipients.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

