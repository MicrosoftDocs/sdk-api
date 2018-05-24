---
UID: NF:faxcomex.IFaxDocument.put_CoverPage
title: IFaxDocument::put_CoverPage
author: windows-driver-content
description: The CoverPage property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document.
old-location: fax\_mfax_faxdocument_coverpage_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9fol.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CoverPage property [Fax Service], CoverPage property [Fax Service],FaxDocument object, FaxDocument object [Fax Service],CoverPage property, FaxDocument.CoverPage, IFaxDocument.put_CoverPage, IFaxDocument::put_CoverPage, _mfax_faxdocument.coverpage, fax._mfax_faxdocument_coverpage, fax._mfax_faxdocument_coverpage_vb, put_CoverPage
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxDocument.CoverPage
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument::put_CoverPage


## -description


The <b>CoverPage</b> property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document.

This property is read/write.


## -parameters


## -remarks



To specify a server-based cover page file, you must set the <a href="https://msdn.microsoft.com/6313301b-06ec-494d-9671-66dc06a2ec1c">CoverPageType</a> property to 2.

                

To specify a local or personal cover page file, you must set the <a href="https://msdn.microsoft.com/6313301b-06ec-494d-9671-66dc06a2ec1c">CoverPageType</a> property to 1.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

