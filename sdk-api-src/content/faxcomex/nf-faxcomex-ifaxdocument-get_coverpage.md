---
UID: NF:faxcomex.IFaxDocument.get_CoverPage
title: IFaxDocument::get_CoverPage (faxcomex.h)
author: windows-sdk-content
description: The IFaxDocument::get_CoverPage property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_coverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9fol.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CoverPage property [Fax Service], CoverPage property [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],CoverPage property, IFaxDocument.CoverPage, IFaxDocument.get_CoverPage, IFaxDocument::CoverPage, IFaxDocument::get_CoverPage, IFaxDocument::put_CoverPage, _mfax_faxdocument.coverpage, fax._mfax_faxdocument_coverpage, fax._mfax_faxdocument_cpp_mfax_faxdocument_coverpage_cpp, faxcomex/IFaxDocument::CoverPage, faxcomex/IFaxDocument::get_CoverPage, faxcomex/IFaxDocument::put_CoverPage, get_CoverPage
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
 - IFaxDocument.CoverPage
 - IFaxDocument.get_CoverPage
 - IFaxDocument.put_CoverPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::get_CoverPage


## -description


The <b>IFaxDocument::get_CoverPage</b> property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document.

This property is read/write.


## -parameters


## -remarks



To specify a server-based cover page file, you must set the <a href="https://msdn.microsoft.com/en-us/library/ms686003(v=VS.85).aspx">IFaxDocument::get_CoverPageType</a> property to <a href="https://msdn.microsoft.com/en-us/library/ms689603(v=VS.85).aspx">fcptSERVER</a>.

                

To specify a local or personal cover page file, you must set the <a href="https://msdn.microsoft.com/en-us/library/ms686003(v=VS.85).aspx">IFaxDocument::get_CoverPageType</a> property to <a href="https://msdn.microsoft.com/en-us/library/ms689603(v=VS.85).aspx">fcptLOCAL</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685960(v=VS.85).aspx">IFaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692936(v=VS.85).aspx">Visual Basic Example</a>
 

 

