---
UID: NF:faxcomex.IFaxDocument.ConnectedSubmit
title: IFaxDocument::ConnectedSubmit
author: windows-sdk-content
description: The ConnectedSubmit method submits a single fax document to the connected FaxServer. The method returns an array of fax job ID strings, one for each recipient of the fax.
old-location: fax\_mfax_faxdocument_connectedsubmit.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5cfo.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ConnectedSubmit, ConnectedSubmit method [Fax Service], ConnectedSubmit method [Fax Service],FaxDocument object, FaxDocument object [Fax Service],ConnectedSubmit method, FaxDocument.ConnectedSubmit, IFaxDocument.ConnectedSubmit, IFaxDocument::ConnectedSubmit, _mfax_faxdocument.connectedsubmit, fax._mfax_faxdocument_connectedsubmit
ms.prod: windows
ms.technology: windows-sdk
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
 - FaxDocument.ConnectedSubmit
 - IFaxDocument.ConnectedSubmit
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDocument::ConnectedSubmit


## -description


The <b>ConnectedSubmit</b> method submits a single fax document to the connected <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a>. The method returns an array of fax job ID strings, one for each recipient of the fax.


## -parameters




### -param pFaxServer




### -param pvFaxOutgoingJobIDs






#### - FaxServer [in]

Type: <b>FaxServer*</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a> object that specifies a connected fax server.


## -returns



Type: <b>Variant*</b>

<b>Variant</b> that holds an array of outbound job ID strings, one for each recipient of the fax.




## -remarks



<div class="alert"><b>Note</b>  To succeed, the <b>ConnectedSubmit</b> method requires that the <a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a> object have at least one recipient, and either a cover page or a fax body. You can only use this method if the server (remote or local) is installed as a network printer on the local computer.</div>
<div> </div>
This method is not supported for a remote connection to a fax server running Windows XP Home Edition or Windows XP Professional, and will return the error: <a href="https://msdn.microsoft.com/en-us/library/ms693490(v=VS.85).aspx">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a>, <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_NORMAL</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_HIGH</a> access right, depending on the <a href="https://msdn.microsoft.com/en-us/library/ms687026(v=VS.85).aspx">Priority</a> of the fax document.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685960(v=VS.85).aspx">IFaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692936(v=VS.85).aspx">Visual Basic Example</a>
 

 

