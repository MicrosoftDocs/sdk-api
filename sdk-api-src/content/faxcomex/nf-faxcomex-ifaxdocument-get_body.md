---
UID: NF:faxcomex.IFaxDocument.get_Body
title: IFaxDocument::get_Body
author: windows-sdk-content
description: The Body property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page.
old-location: fax\_mfax_faxdocument_body_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1d6h.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: Body property [Fax Service], Body property [Fax Service],FaxDocument object, FaxDocument object [Fax Service],Body property, FaxDocument.Body, IFaxDocument.get_Body, IFaxDocument::get_Body, _mfax_faxdocument.body, fax._mfax_faxdocument_body, fax._mfax_faxdocument_body_vb, get_Body
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
 - FaxDocument.Body
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument::get_Body


## -description


The <b>Body</b> property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page.

This property is read/write.


## -parameters


## -remarks



Examples of documents that you can send as a fax body are a text file (.txt), a Microsoft Word document (.doc), or a Microsoft Excel spreadsheet (.xls). When you send a fax from a client computer, the body has to be associated with an application that is installed on that computer, and the application has to support the <b>PrintTo</b> verb; otherwise, the fax will fail.

Either the <a href="https://msdn.microsoft.com/c5e0fd2b-9d64-4854-954e-a6e7557f6d3d">Bodies</a> property or the <b>Body</b> property must be <b>NULL</b>. You must use <b>Bodies</b> if you will be submitting with either <a href="https://msdn.microsoft.com/6a62e987-8853-41f0-b440-1571e761ac75">ConnectedSubmit2</a> or <a href="https://msdn.microsoft.com/6adffb23-0a42-4846-b60d-dcdfc9ef63b6">Submit2</a> (both available only in Windows Vista or later). You must use <b>Body</b> if you will be submitting with either <a href="https://msdn.microsoft.com/61bf59fd-b921-4356-a3ab-4b83757cc346">ConnectedSubmit</a> or <a href="https://msdn.microsoft.com/50062e89-9e97-43aa-bb60-7ddf6448585d">Submit</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

