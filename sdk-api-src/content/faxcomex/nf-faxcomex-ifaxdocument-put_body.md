---
UID: NF:faxcomex.IFaxDocument.put_Body
title: IFaxDocument::put_Body
author: windows-sdk-content
description: The IFaxDocument::get_Body property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_body_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1d6h.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Body property [Fax Service], Body property [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],Body property, IFaxDocument.Body, IFaxDocument.put_Body, IFaxDocument::Body, IFaxDocument::get_Body, IFaxDocument::put_Body, _mfax_faxdocument.body, fax._mfax_faxdocument_body, fax._mfax_faxdocument_cpp_mfax_faxdocument_body_cpp, faxcomex/IFaxDocument::Body, faxcomex/IFaxDocument::get_Body, faxcomex/IFaxDocument::put_Body, put_Body
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
 - IFaxDocument.Body
 - IFaxDocument.get_Body
 - IFaxDocument.put_Body
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::put_Body


## -description


The <b>IFaxDocument::get_Body</b> property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page.

This property is read/write.


## -parameters


## -remarks



Examples of documents that you can send as a fax body are a text file (.txt), a Microsoft Word document (.doc), or a Microsoft Excel spreadsheet (.xls). When you send a fax from a client computer, the body has to be associated with an application that is installed on that computer, and the application has to support the <b>PrintTo</b> verb; otherwise, the fax will fail.

Either the <a href="https://msdn.microsoft.com/c985862e-6681-4cc3-b559-ba8ae512389b">Bodies</a> property or the <b>IFaxDocument::get_Body</b> property must be <b>NULL</b>. You must use <b>Bodies</b> if you will be submitting with either <a href="https://msdn.microsoft.com/95d13f50-59fd-4f17-877e-83b51deb9b6c">ConnectedSubmit2</a> or <a href="https://msdn.microsoft.com/63deca4c-a248-4f77-9cd6-6b1d845b6236">Submit2</a> (both available only in Windows Vista or later). You must use <b>IFaxDocument::get_Body</b> if you will be submitting with either <a href="https://msdn.microsoft.com/61bf59fd-b921-4356-a3ab-4b83757cc346">ConnectedSubmit</a> or <a href="https://msdn.microsoft.com/46dab8a7-157a-4869-b64e-2eebca19bdae">IFaxDocument::Submit</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

