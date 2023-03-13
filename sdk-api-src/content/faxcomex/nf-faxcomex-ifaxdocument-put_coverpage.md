---
UID: NF:faxcomex.IFaxDocument.put_CoverPage
title: IFaxDocument::put_CoverPage (faxcomex.h)
description: The IFaxDocument::get_CoverPage property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document. (Put)
helpviewer_keywords: ["CoverPage property [Fax Service]","CoverPage property [Fax Service]","IFaxDocument interface","IFaxDocument interface [Fax Service]","CoverPage property","IFaxDocument.CoverPage","IFaxDocument.put_CoverPage","IFaxDocument::CoverPage","IFaxDocument::get_CoverPage","IFaxDocument::put_CoverPage","_mfax_faxdocument.coverpage","fax._mfax_faxdocument_coverpage","fax._mfax_faxdocument_cpp_mfax_faxdocument_coverpage_cpp","faxcomex/IFaxDocument::CoverPage","faxcomex/IFaxDocument::get_CoverPage","faxcomex/IFaxDocument::put_CoverPage","put_CoverPage"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_coverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9fol.htm
ms.date: 12/05/2018
ms.keywords: CoverPage property [Fax Service], CoverPage property [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],CoverPage property, IFaxDocument.CoverPage, IFaxDocument.put_CoverPage, IFaxDocument::CoverPage, IFaxDocument::get_CoverPage, IFaxDocument::put_CoverPage, _mfax_faxdocument.coverpage, fax._mfax_faxdocument_coverpage, fax._mfax_faxdocument_cpp_mfax_faxdocument_coverpage_cpp, faxcomex/IFaxDocument::CoverPage, faxcomex/IFaxDocument::get_CoverPage, faxcomex/IFaxDocument::put_CoverPage, put_CoverPage
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
 - IFaxDocument::put_CoverPage
 - faxcomex/IFaxDocument::put_CoverPage
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
 - IFaxDocument.CoverPage
 - IFaxDocument.get_CoverPage
 - IFaxDocument.put_CoverPage
---

# IFaxDocument::put_CoverPage


## -description

The <b>IFaxDocument::get_CoverPage</b> property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document.

This property is read/write.

## -parameters

## -remarks

To specify a server-based cover page file, you must set the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-coverpagetype-vb">IFaxDocument::get_CoverPageType</a> property to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_coverpage_type_enum">fcptSERVER</a>.

                

To specify a local or personal cover page file, you must set the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-coverpagetype-vb">IFaxDocument::get_CoverPageType</a> property to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_coverpage_type_enum">fcptLOCAL</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
