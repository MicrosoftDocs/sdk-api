---
UID: NF:faxcomex.IFaxDocument2.put_Bodies
title: IFaxDocument2::put_Bodies (faxcomex.h)
author: windows-sdk-content
description: Provides a collection of one or more documents to the fax document.
old-location: fax\_mfax_faxdocument2_cpp_mfax_faxdocument2_bodies_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\bodies.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Bodies property [Fax Service], Bodies property [Fax Service],IFaxDocument2 interface, IFaxDocument2 interface [Fax Service],Bodies property, IFaxDocument2.Bodies, IFaxDocument2.put_Bodies, IFaxDocument2::Bodies, IFaxDocument2::get_Bodies, IFaxDocument2::put_Bodies, _mfax_faxdocument2.bodies, fax._mfax_faxdocument2_bodies, fax._mfax_faxdocument2_cpp_mfax_faxdocument2_bodies_cpp, faxcomex/IFaxDocument2::Bodies, faxcomex/IFaxDocument2::get_Bodies, faxcomex/IFaxDocument2::put_Bodies, put_Bodies
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
 - IFaxDocument2.Bodies
 - IFaxDocument2.get_Bodies
 - IFaxDocument2.put_Bodies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDocument2::put_Bodies


## -description


Provides a collection of one or more documents to the fax document. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



Examples of documents that you can send as fax bodies include text files (.txt), Microsoft Word documents (.doc), or Microsoft Excel spreadsheets (.xls). Filenames are separated with semi-colons ";". For example, "myfile.txt;anotherfile.doc".

Either the <b>IFaxDocument2::Bodies</b> property or the <a href="https://msdn.microsoft.com/en-us/library/ms684817(v=VS.85).aspx">Body</a> property must be <b>NULL</b>. You must use <b>IFaxDocument2::Bodies</b> if you will be submitting using either <a href="https://msdn.microsoft.com/en-us/library/Aa359009(v=VS.85).aspx">IFaxDocument2::ConnectedSubmit2</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa359012(v=VS.85).aspx">IFaxDocument2::Submit2</a> (both available only in Windows Vista or later). You must use <b>Body</b> if you will be submitting using either <a href="https://msdn.microsoft.com/en-us/library/ms686178(v=VS.85).aspx">ConnectedSubmit</a> or <a href="https://msdn.microsoft.com/en-us/library/ms687477(v=VS.85).aspx">Submit</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359010(v=VS.85).aspx">IFaxDocument2</a>
 

 

