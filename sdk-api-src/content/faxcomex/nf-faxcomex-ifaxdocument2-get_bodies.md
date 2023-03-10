---
UID: NF:faxcomex.IFaxDocument2.get_Bodies
title: IFaxDocument2::get_Bodies (faxcomex.h)
description: Provides a collection of one or more documents to the fax document. (Get)
helpviewer_keywords: ["Bodies property [Fax Service]","Bodies property [Fax Service]","IFaxDocument2 interface","IFaxDocument2 interface [Fax Service]","Bodies property","IFaxDocument2.Bodies","IFaxDocument2.get_Bodies","IFaxDocument2::Bodies","IFaxDocument2::get_Bodies","IFaxDocument2::put_Bodies","_mfax_faxdocument2.bodies","fax._mfax_faxdocument2_bodies","fax._mfax_faxdocument2_cpp_mfax_faxdocument2_bodies_cpp","faxcomex/IFaxDocument2::Bodies","faxcomex/IFaxDocument2::get_Bodies","faxcomex/IFaxDocument2::put_Bodies","get_Bodies"]
old-location: fax\_mfax_faxdocument2_cpp_mfax_faxdocument2_bodies_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\bodies.htm
ms.date: 12/05/2018
ms.keywords: Bodies property [Fax Service], Bodies property [Fax Service],IFaxDocument2 interface, IFaxDocument2 interface [Fax Service],Bodies property, IFaxDocument2.Bodies, IFaxDocument2.get_Bodies, IFaxDocument2::Bodies, IFaxDocument2::get_Bodies, IFaxDocument2::put_Bodies, _mfax_faxdocument2.bodies, fax._mfax_faxdocument2_bodies, fax._mfax_faxdocument2_cpp_mfax_faxdocument2_bodies_cpp, faxcomex/IFaxDocument2::Bodies, faxcomex/IFaxDocument2::get_Bodies, faxcomex/IFaxDocument2::put_Bodies, get_Bodies
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
 - IFaxDocument2::get_Bodies
 - faxcomex/IFaxDocument2::get_Bodies
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
 - IFaxDocument2.Bodies
 - IFaxDocument2.get_Bodies
 - IFaxDocument2.put_Bodies
---

# IFaxDocument2::get_Bodies


## -description

Provides a collection of one or more documents to the fax document. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.

## -parameters

## -remarks

Examples of documents that you can send as fax bodies include text files (.txt), Microsoft Word documents (.doc), or Microsoft Excel spreadsheets (.xls). Filenames are separated with semi-colons ";". For example, "myfile.txt;anotherfile.doc".

Either the <b>IFaxDocument2::Bodies</b> property or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-body-vb">Body</a> property must be <b>NULL</b>. You must use <b>IFaxDocument2::Bodies</b> if you will be submitting using either <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-connectedsubmit2-vb">IFaxDocument2::ConnectedSubmit2</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-submit2-vb">IFaxDocument2::Submit2</a> (both available only in Windows Vista or later). You must use <b>Body</b> if you will be submitting using either <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-connectedsubmit">ConnectedSubmit</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-submit-vb">Submit</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument2">IFaxDocument2</a>
