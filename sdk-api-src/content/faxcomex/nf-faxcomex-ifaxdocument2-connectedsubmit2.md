---
UID: NF:faxcomex.IFaxDocument2.ConnectedSubmit2
title: IFaxDocument2::ConnectedSubmit2
author: windows-sdk-content
description: Submits one or more fax documents to the connected FaxServer.
old-location: fax\_mfax_faxdocument2_connectedsubmit2_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\connectedsubmit2.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ConnectedSubmit2, ConnectedSubmit2 method [Fax Service], ConnectedSubmit2 method [Fax Service],FaxDocument object, FaxDocument object [Fax Service],ConnectedSubmit2 method, FaxDocument.ConnectedSubmit2, IFaxDocument2.ConnectedSubmit2, IFaxDocument2::ConnectedSubmit2, _mfax_faxdocument2.connectedsubmit2, fax._mfax_faxdocument2_connectedsubmit2, fax._mfax_faxdocument2_connectedsubmit2_vb
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
 - FaxDocument.ConnectedSubmit2
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

