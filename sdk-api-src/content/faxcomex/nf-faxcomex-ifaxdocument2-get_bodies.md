---
UID: NF:faxcomex.IFaxDocument2.get_Bodies
title: IFaxDocument2::get_Bodies method
author: windows-driver-content
description: Provides a collection of one or more documents to the fax document.
old-location: fax\_mfax_faxdocument2_bodies_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\bodies.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: Bodies property [Fax Service], Bodies property [Fax Service], FaxDocument object, FaxDocument object [Fax Service], Bodies property, IFaxDocument2, IFaxDocument2::get_Bodies, _mfax_faxdocument2.bodies, fax._mfax_faxdocument2_bodies, fax._mfax_faxdocument2_bodies_vb, get_Bodies,IFaxDocument2.get_Bodies
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxDocument.Bodies
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument2::get_Bodies method


## -description


Provides a collection of one or more documents to the fax document. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



Examples of documents that you can send as fax bodies include text files (.txt), Microsoft Word documents (.doc), or Microsoft Excel spreadsheets (.xls). Filenames are separated with semi-colons ";". For example, "myfile.txt;anotherfile.doc".

Either the <b>Bodies</b> property or the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545226">Body</a> property must be <b>NULL</b>. You must use <b>Bodies</b> if you will be submitting using either <a href="https://msdn.microsoft.com/6a62e987-8853-41f0-b440-1571e761ac75">ConnectedSubmit2</a> or <a href="https://msdn.microsoft.com/6adffb23-0a42-4846-b60d-dcdfc9ef63b6">Submit2</a> (both available only in Windows Vista or later). You must use <b>Body</b> if you will be submitting using either <a href="https://msdn.microsoft.com/61bf59fd-b921-4356-a3ab-4b83757cc346">ConnectedSubmit</a> or <a href="https://msdn.microsoft.com/50062e89-9e97-43aa-bb60-7ddf6448585d">Submit</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/20b98e3e-3126-4be1-b9af-228164d0bda6">IFaxDocument2</a>
 

 

