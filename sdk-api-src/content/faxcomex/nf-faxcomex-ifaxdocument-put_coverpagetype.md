---
UID: NF:faxcomex.IFaxDocument.put_CoverPageType
title: IFaxDocument::put_CoverPageType method
author: windows-driver-content
description: The CoverPageType property is a value from an enumeration that indicates whether a specified cover page template file (.cov) is a server-based cover page file or a local-computer-based cover page file. You can also specify that no file is used.
old-location: fax\_mfax_faxdocument_coverpagetype_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3v8l.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: CoverPageType property [Fax Service], CoverPageType property [Fax Service], FaxDocument object, FaxDocument object [Fax Service], CoverPageType property, IFaxDocument, IFaxDocument::put_CoverPageType, _mfax_faxdocument.coverpagetype, fax._mfax_faxdocument_coverpagetype, fax._mfax_faxdocument_coverpagetype_vb, put_CoverPageType,IFaxDocument.put_CoverPageType
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
-	FaxDocument.CoverPageType
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument::put_CoverPageType method


## -description


The <b>CoverPageType</b> property is a value from an enumeration that indicates whether a specified cover page template file (.cov) is a server-based cover page file or a local-computer-based cover page file. You can also specify that no file is used.

This property is read/write.


## -parameters


## -remarks



By default, <b>CoverPageType</b> is set to 0, indicating that no file is used.

Provide the name of the cover page in the <a href="https://msdn.microsoft.com/ae883970-dfd4-4811-b5a6-c666e1289707">CoverPage</a> property.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

