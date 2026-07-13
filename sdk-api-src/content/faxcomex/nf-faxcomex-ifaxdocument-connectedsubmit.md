---
UID: NF:faxcomex.IFaxDocument.ConnectedSubmit
title: IFaxDocument::ConnectedSubmit (faxcomex.h)
description: The IFaxDocument::ConnectedSubmit method submits a single fax document to the connected IFaxServer. The method returns an array of fax job ID strings, one for each recipient of the fax.
helpviewer_keywords: ["ConnectedSubmit","ConnectedSubmit method [Fax Service]","ConnectedSubmit method [Fax Service]","IFaxDocument interface","IFaxDocument interface [Fax Service]","ConnectedSubmit method","IFaxDocument.ConnectedSubmit","IFaxDocument::ConnectedSubmit","_mfax_faxdocument.connectedsubmit_cpp","fax._mfax_faxdocument_connectedsubmit_cpp","faxcomex/IFaxDocument::ConnectedSubmit"]
old-location: fax\_mfax_faxdocument_connectedsubmit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5cfo_cpp.htm
ms.date: 12/05/2018
ms.keywords: ConnectedSubmit, ConnectedSubmit method [Fax Service], ConnectedSubmit method [Fax Service],IFaxDocument interface, IFaxDocument interface [Fax Service],ConnectedSubmit method, IFaxDocument.ConnectedSubmit, IFaxDocument::ConnectedSubmit, _mfax_faxdocument.connectedsubmit_cpp, fax._mfax_faxdocument_connectedsubmit_cpp, faxcomex/IFaxDocument::ConnectedSubmit
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
 - IFaxDocument::ConnectedSubmit
 - faxcomex/IFaxDocument::ConnectedSubmit
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
 - IFaxDocument.ConnectedSubmit
---

# IFaxDocument::ConnectedSubmit


## -description

The <b>IFaxDocument::ConnectedSubmit</b> method submits a single fax document to the connected <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>. The method returns an array of fax job ID strings, one for each recipient of the fax.

## -parameters

### -param pFaxServer [in]

Type: <b>IFaxServer*</b>

An <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a> interface that specifies a connected fax server.

### -param pvFaxOutgoingJobIDs [out, retval]

Type: <b>VARIANT*</b>

<b>VARIANT</b> that holds an array of outbound job ID strings, one for each recipient of the fax.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  To succeed, the <b>IFaxDocument::ConnectedSubmit</b> method requires that the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a> object have at least one recipient, and either a cover page or a fax body. You can only use this method if the server (remote or local) is installed as a network printer on the local computer.</div>
<div> </div>
This method is not supported for a remote connection to a fax server running Windows XP Home Edition or Windows XP Professional, and will return the error: <a href="/previous-versions/windows/desktop/fax/-mfax-fax-error-codes">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a>, <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_NORMAL</a>, or <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_HIGH</a> access right, depending on the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-priority-vb">IFaxDocument::get_Priority</a> of the fax document.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>