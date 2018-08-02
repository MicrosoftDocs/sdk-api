---
UID: NF:faxcomex.IFaxDocument2.get_Bodies
title: IFaxDocument2::get_Bodies
author: windows-sdk-content
description: Provides a collection of one or more documents to the fax document.
old-location: fax\_mfax_faxdocument2_bodies_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\bodies.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: Bodies property [Fax Service], Bodies property [Fax Service],FaxDocument object, FaxDocument object [Fax Service],Bodies property, FaxDocument.Bodies, IFaxDocument2.get_Bodies, IFaxDocument2::get_Bodies, _mfax_faxdocument2.bodies, fax._mfax_faxdocument2_bodies, fax._mfax_faxdocument2_bodies_vb, get_Bodies
ms.prod: windows
ms.technology: windows-sdk
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
 - FaxDocument.Bodies
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument2::get_Bodies


## -description


Provides a collection of one or more documents to the fax document. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



Examples of documents that you can send as fax bodies include text files (.txt), Microsoft Word documents (.doc), or Microsoft Excel spreadsheets (.xls). Filenames are separated with semi-colons ";". For example, "myfile.txt;anotherfile.doc".

Either the <b>Bodies</b> property or the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545226">Body</a> property must be <b>NULL</b>. You must use <b>Bodies</b> if you will be submitting using either <a href="https://msdn.microsoft.com/en-us/library/Aa359009(v=VS.85).aspx">ConnectedSubmit2</a> or <a href="https://msdn.microsoft.com/library/Aa359012(v=VS.85).aspx">Submit2</a> (both available only in Windows Vista or later). You must use <b>Body</b> if you will be submitting using either <a href="https://msdn.microsoft.com/library/ms686178(v=VS.85).aspx">ConnectedSubmit</a> or <a href="https://msdn.microsoft.com/library/ms687477(v=VS.85).aspx">Submit</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/ms685958(v=VS.85).aspx">FaxDocument</a>



<a href="https://msdn.microsoft.com/library/Aa359010(v=VS.85).aspx">IFaxDocument2</a>
 

 

