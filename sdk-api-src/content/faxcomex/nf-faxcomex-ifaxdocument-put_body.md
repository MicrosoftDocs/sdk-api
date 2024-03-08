---
UID: NF:faxcomex.IFaxDocument.put_Body
title: IFaxDocument::put_Body (faxcomex.h)
description: The IFaxDocument::get_Body property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page. (Put)
helpviewer_keywords: ["Body property [Fax Service]","Body property [Fax Service]","IFaxDocument interface","IFaxDocument interface [Fax Service]","Body property","IFaxDocument.Body","IFaxDocument.put_Body","IFaxDocument::Body","IFaxDocument::get_Body","IFaxDocument::put_Body","_mfax_faxdocument.body","fax._mfax_faxdocument_body","fax._mfax_faxdocument_cpp_mfax_faxdocument_body_cpp","faxcomex/IFaxDocument::Body","faxcomex/IFaxDocument::get_Body","faxcomex/IFaxDocument::put_Body","put_Body"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_body_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1d6h.htm
ms.date: 12/05/2018
ms.keywords: Body property [Fax Service], Body property [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],Body property, IFaxDocument.Body, IFaxDocument.put_Body, IFaxDocument::Body, IFaxDocument::get_Body, IFaxDocument::put_Body, _mfax_faxdocument.body, fax._mfax_faxdocument_body, fax._mfax_faxdocument_cpp_mfax_faxdocument_body_cpp, faxcomex/IFaxDocument::Body, faxcomex/IFaxDocument::get_Body, faxcomex/IFaxDocument::put_Body, put_Body
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
 - IFaxDocument::put_Body
 - faxcomex/IFaxDocument::put_Body
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
 - IFaxDocument.Body
 - IFaxDocument.get_Body
 - IFaxDocument.put_Body
---

# IFaxDocument::put_Body


## -description

The <b>IFaxDocument::get_Body</b> property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page.

This property is read/write.

## -parameters

## -remarks

Examples of documents that you can send as a fax body are a text file (.txt), a Microsoft Word document (.doc), or a Microsoft Excel spreadsheet (.xls). When you send a fax from a client computer, the body has to be associated with an application that is installed on that computer, and the application has to support the <b>PrintTo</b> verb; otherwise, the fax will fail.

Either the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-bodies-vb">Bodies</a> property or the <b>IFaxDocument::get_Body</b> property must be <b>NULL</b>. You must use <b>Bodies</b> if you will be submitting with either <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-connectedsubmit2-vb">ConnectedSubmit2</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-submit2-vb">Submit2</a> (both available only in Windows Vista or later). You must use <b>IFaxDocument::get_Body</b> if you will be submitting with either <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-connectedsubmit">ConnectedSubmit</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-submit-vb">IFaxDocument::Submit</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
