---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFaxDocument2::get_Bodies


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
 

 

