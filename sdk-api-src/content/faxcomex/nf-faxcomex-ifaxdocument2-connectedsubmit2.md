---
UID: NF:faxcomex.IFaxDocument2.ConnectedSubmit2
title: IFaxDocument2::ConnectedSubmit2 (faxcomex.h)
description: Submits one or more fax documents to the connected FaxServer.
helpviewer_keywords: ["ConnectedSubmit2","ConnectedSubmit2 method [Fax Service]","ConnectedSubmit2 method [Fax Service]","IFaxDocument2 interface","IFaxDocument2 interface [Fax Service]","ConnectedSubmit2 method","IFaxDocument2.ConnectedSubmit2","IFaxDocument2::ConnectedSubmit2","_mfax_faxdocument2.connectedsubmit2","fax._mfax_faxdocument2_connectedsubmit2","fax._mfax_faxdocument2_cpp_mfax_faxdocument2_connectedsubmit2_cpp","faxcomex/IFaxDocument2::ConnectedSubmit2"]
old-location: fax\_mfax_faxdocument2_cpp_mfax_faxdocument2_connectedsubmit2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\connectedsubmit2.htm
ms.date: 12/05/2018
ms.keywords: ConnectedSubmit2, ConnectedSubmit2 method [Fax Service], ConnectedSubmit2 method [Fax Service],IFaxDocument2 interface, IFaxDocument2 interface [Fax Service],ConnectedSubmit2 method, IFaxDocument2.ConnectedSubmit2, IFaxDocument2::ConnectedSubmit2, _mfax_faxdocument2.connectedsubmit2, fax._mfax_faxdocument2_connectedsubmit2, fax._mfax_faxdocument2_cpp_mfax_faxdocument2_connectedsubmit2_cpp, faxcomex/IFaxDocument2::ConnectedSubmit2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDocument2::ConnectedSubmit2
 - faxcomex/IFaxDocument2::ConnectedSubmit2
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
 - IFaxDocument2.ConnectedSubmit2
---

# IFaxDocument2::ConnectedSubmit2


## -description

Submits one or more fax documents to the connected <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>. This method returns an array of fax job ID strings, one for each recipient of the fax.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters

### -param pFaxServer [in]

Type: <b>IFaxServer*</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a> object that specifies a connected fax server.

### -param pvFaxOutgoingJobIDs [out]

Type: <b>VARIANT*</b>

A <b>VARIANT</b> that holds an array of outbound job ID strings, one for each recipient of the fax.

### -param plErrorBodyFile [out, retval]

Type: <b>LONG*</b>

A <b>LONG</b> representing the zero-based position of the submitted file that caused the fax send operation to fail. See Remarks.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  To succeed, the <b>IFaxDocument2::ConnectedSubmit2</b> method requires that the fax have at least one recipient, and either a cover page or a fax body. You can only use this method if the server (remote or local) is installed as a network printer on the local computer.</div>
<div> </div>
You must set the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-bodies-vb">IFaxDocument2::Bodies</a> property with a semi-colon delimited list of the files to be faxed before calling <b>IFaxDocument2::ConnectedSubmit2</b>. 



<div class="alert"><b>Note</b>  The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-body-vb">Body</a> property must be <b>NULL</b> to use <b>IFaxDocument2::ConnectedSubmit2</b>.</div>
<div> </div>
This method is not supported for a remote connection to a fax server running Windows XP Home Edition or Windows XP Professional, and will return the error: <a href="/previous-versions/windows/desktop/fax/-mfax-fax-error-codes">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_LOW</a>, <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_NORMAL</a>, or <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_HIGH</a> access set correctly, depending on the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-priority-vb">Priority</a> of the fax document.

To illustrate <i>plErrorBodyFile</i>, here is an example: The following list of files is submitted as the value of <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument2-bodies-vb">IFaxDocument2::Bodies</a>:

"MyTextFile.txt;AnotherTextFile.txt;MyPDFfile.pdf;MyWordFile.doc".

Because the "*.pdf" extension is not supported, the send operation will fail and <i>plErrorBodyFile</i> will return as 2.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument2">IFaxDocument2</a>