---
UID: NF:faxcomex.IFaxDocument.Submit
title: IFaxDocument::Submit
author: windows-sdk-content
description: The IFaxDocument::Submit method submits a single fax document to the fax service for processing.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_submit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_97w4.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxDocument interface [Fax Service],Submit method, IFaxDocument.Submit, IFaxDocument::Submit, Submit, Submit method [Fax Service], Submit method [Fax Service],IFaxDocument interface, _mfax_faxdocument.submit, fax._mfax_faxdocument_cpp_mfax_faxdocument_submit_cpp, fax._mfax_faxdocument_submit, faxcomex/IFaxDocument::Submit
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
 - IFaxDocument.Submit
 - IFaxDocument.Submit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::Submit


## -description


The <b>IFaxDocument::Submit</b> method submits a single fax document to the fax service for processing.


## -parameters




### -param bstrFaxServerName [in]

Type: <b>BSTR</b>

<b>BSTR</b> that specifies a fax server. If this parameter is <b>NULL</b> or an empty string, the local fax server is specified.


### -param pvFaxOutgoingJobIDs

TBD




#### - vFaxOutgoingJobIDs [out, retval]

Type: <b>VARIANT*</b>

<b>VARIANT</b> that specifies a collection of outbound job IDs, one for each recipient of the fax.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must provide the server name when submitting the document. To submit the document to the local server, set the <i>bstrFaxServerName</i> parameter to <b>NULL</b> or an empty string. The method returns a collection of fax job IDs, one for each recipient of the fax.

To succeed, the <b>IFaxDocument::Submit</b> method requires that the <a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a> interface have at least one recipient, and either a cover page or a fax body. You can only use this method if the server (remote or local) is installed as a network printer on the local computer.

This method is not supported for a remote connection to a fax server running Windows XP Home Edition or Windows XP Professional, and will return the error <a href="https://msdn.microsoft.com/b5d59fec-2802-40bd-8ce4-748137f30fb2">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a>, <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_NORMAL</a>, or <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_HIGH</a> access right, depending on the <a href="https://msdn.microsoft.com/4f7ebcad-ff7d-4c11-b4c4-c7325415231e">Priority</a> of the fax document.




## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/82a9e599-35d3-4fca-954f-dbc579c023f5">Visual Basic Example</a>
 

 

