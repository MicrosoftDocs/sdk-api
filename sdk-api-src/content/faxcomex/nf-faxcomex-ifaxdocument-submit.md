---
UID: NF:faxcomex.IFaxDocument.Submit
title: IFaxDocument::Submit (faxcomex.h)
description: The IFaxDocument::Submit method submits a single fax document to the fax service for processing.
helpviewer_keywords: ["IFaxDocument interface [Fax Service]","Submit method","IFaxDocument.Submit","IFaxDocument::Submit","Submit","Submit method [Fax Service]","Submit method [Fax Service]","IFaxDocument interface","_mfax_faxdocument.submit","fax._mfax_faxdocument_cpp_mfax_faxdocument_submit_cpp","fax._mfax_faxdocument_submit","faxcomex/IFaxDocument::Submit"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_submit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_97w4.htm
ms.date: 12/05/2018
ms.keywords: IFaxDocument interface [Fax Service],Submit method, IFaxDocument.Submit, IFaxDocument::Submit, Submit, Submit method [Fax Service], Submit method [Fax Service],IFaxDocument interface, _mfax_faxdocument.submit, fax._mfax_faxdocument_cpp_mfax_faxdocument_submit_cpp, fax._mfax_faxdocument_submit, faxcomex/IFaxDocument::Submit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDocument::Submit
 - faxcomex/IFaxDocument::Submit
dev_langs:
 - c++
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
---

# IFaxDocument::Submit


## -description

The <b>IFaxDocument::Submit</b> method submits a single fax document to the fax service for processing.

## -parameters

### -param bstrFaxServerName [in]

Type: <b>BSTR</b>

<b>BSTR</b> that specifies a fax server. If this parameter is <b>NULL</b> or an empty string, the local fax server is specified.

### -param pvFaxOutgoingJobIDs

Type: <b>VARIANT*</b>

<b>VARIANT</b> that specifies a collection of outbound job IDs, one for each recipient of the fax.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must provide the server name when submitting the document. To submit the document to the local server, set the <i>bstrFaxServerName</i> parameter to <b>NULL</b> or an empty string. The method returns a collection of fax job IDs, one for each recipient of the fax.

To succeed, the <b>IFaxDocument::Submit</b> method requires that the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a> interface have at least one recipient, and either a cover page or a fax body. You can only use this method if the server (remote or local) is installed as a network printer on the local computer.

This method is not supported for a remote connection to a fax server running Windows XP Home Edition or Windows XP Professional, and will return the error <a href="/previous-versions/windows/desktop/fax/-mfax-fax-error-codes">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a>, <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_NORMAL</a>, or <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_HIGH</a> access right, depending on the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-priority-vb">Priority</a> of the fax document.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-broadcasting-a-fax">Visual Basic Example</a>