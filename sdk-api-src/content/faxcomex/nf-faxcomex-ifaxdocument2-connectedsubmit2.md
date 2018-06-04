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

# IFaxDocument2::ConnectedSubmit2


## -description


Submits one or more fax documents to the connected <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>. This method returns an array of fax job ID strings, one for each recipient of the fax.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters




### -param pFaxServer [in]

Type: <b>IFaxServer*</b>

A <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object that specifies a connected fax server.


### -param pvFaxOutgoingJobIDs [out]

Type: <b>Variant*</b>

A <b>Variant</b> that holds an array of outbound job ID strings, one for each recipient of the fax.


### -param plErrorBodyFile






## -returns



Type: <b>Long*</b>

A <b>Long</b> representing the zero-based position of the submitted file that caused the fax send operation to fail. See Remarks.




## -remarks



<div class="alert"><b>Note</b>  To succeed, the <b>ConnectedSubmit2</b> method requires that the fax have at least one recipient, and either a cover page or a fax body. You can only use this method if the server (remote or local) is installed as a network printer on the local computer.</div>
<div> </div>
You must set the <a href="https://msdn.microsoft.com/c5e0fd2b-9d64-4854-954e-a6e7557f6d3d">Bodies</a> property with a semi-colon delimited list of the files to be faxed before calling <b>ConnectedSubmit2</b>. 



<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/library/windows/hardware/ff545226">Body</a> property must be <b>NULL</b> to use <b>ConnectedSubmit2</b>.</div>
<div> </div>
This method is not supported for a remote connection to a fax server running Windows XP Home Edition or Windows XP Professional, and will return the error: <a href="https://msdn.microsoft.com/b5d59fec-2802-40bd-8ce4-748137f30fb2">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_LOW</a>, <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_NORMAL</a>, or <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_HIGH</a> access set correctly, depending on the <a href="https://msdn.microsoft.com/e3dc385d-51e6-4174-b1a5-ff48bde19995">Priority</a> of the fax document.

To illustrate <i>plErrorBodyFile</i>, here is an example: The following list of files is submitted as the value of <a href="https://msdn.microsoft.com/c5e0fd2b-9d64-4854-954e-a6e7557f6d3d">Bodies</a>:

"MyTextFile.txt;AnotherTextFile.txt;MyPDFfile.pdf;MyWordFile.doc".

Because the "*.pdf" extension is not supported, the send operation will fail and <i>plErrorBodyFile</i> will return as 2.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/20b98e3e-3126-4be1-b9af-228164d0bda6">IFaxDocument2</a>
 

 

