---
UID: NF:faxcomex.IFaxIncomingMessage2.ReAssign
title: IFaxIncomingMessage2::ReAssign (faxcomex.h)
description: Reassign the fax to one or more recipients. It also commits changes to the IFaxIncomingMessage2::Subject, IFaxIncomingMessage2::SenderName, IFaxIncomingMessage2::SenderFaxNumber, and IFaxIncomingMessage2::HasCoverPage properties.
helpviewer_keywords: ["IFaxIncomingMessage2 interface [Fax Service]","Reassign method","IFaxIncomingMessage2.ReAssign","IFaxIncomingMessage2.Reassign","IFaxIncomingMessage2::ReAssign","IFaxIncomingMessage2::Reassign","ReAssign","Reassign method [Fax Service]","Reassign method [Fax Service]","IFaxIncomingMessage2 interface","_mfax_faxincomingmessage.reassign","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_reassign_cpp","fax._mfax_faxincomingmessage_reassign","faxcomex/IFaxIncomingMessage2::Reassign"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_reassign_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\reassign.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Reassign method, IFaxIncomingMessage2.ReAssign, IFaxIncomingMessage2.Reassign, IFaxIncomingMessage2::ReAssign, IFaxIncomingMessage2::Reassign, ReAssign, Reassign method [Fax Service], Reassign method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.reassign, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_reassign_cpp, fax._mfax_faxincomingmessage_reassign, faxcomex/IFaxIncomingMessage2::Reassign
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
 - IFaxIncomingMessage2::ReAssign
 - faxcomex/IFaxIncomingMessage2::ReAssign
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
 - IFaxIncomingMessage2.Reassign
 - IFaxIncomingMessage2.Reassign
---

# IFaxIncomingMessage2::ReAssign


## -description

<a href="/previous-versions/windows/desktop/fax/-mfax-glossary">Reassign</a> the fax to one or more recipients. It also commits changes to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">IFaxIncomingMessage2::Subject</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">IFaxIncomingMessage2::SenderName</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">IFaxIncomingMessage2::HasCoverPage</a> properties.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_RECEIVE_FOLDER</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access rights. Also, IFaxConfiguration::IncomingFaxesArePublic must be set to false.

If the <a href="/previous-versions/windows/desktop/fax/-mfax-glossary">routing assistant</a> application is going to set the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">IFaxIncomingMessage2::Subject</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">IFaxIncomingMessage2::SenderName</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">IFaxIncomingMessage2::SenderFaxNumber</a>, or <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">IFaxIncomingMessage2::HasCoverPage</a> properties, it should do this before calling <b>IFaxIncomingMessage2::Reassign</b>. <b>Reassign</b> will commit those changes, so it is not necessary to call <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-save-vb">IFaxIncomingMessage2::Save</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
