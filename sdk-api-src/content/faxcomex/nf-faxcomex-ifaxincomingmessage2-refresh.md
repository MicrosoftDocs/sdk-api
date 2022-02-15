---
UID: NF:faxcomex.IFaxIncomingMessage2.Refresh
title: IFaxIncomingMessage2::Refresh (faxcomex.h)
description: Refreshes FaxIncomingMessage object information from the fax server.
helpviewer_keywords: ["IFaxIncomingMessage2 interface [Fax Service]","Refresh method","IFaxIncomingMessage2.Refresh","IFaxIncomingMessage2::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxIncomingMessage2 interface","_mfax_faxincomingmessage.refresh","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp","fax._mfax_faxincomingmessage_refresh","faxcomex/IFaxIncomingMessage2::Refresh"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\refresh.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Refresh method, IFaxIncomingMessage2.Refresh, IFaxIncomingMessage2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.refresh, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp, fax._mfax_faxincomingmessage_refresh, faxcomex/IFaxIncomingMessage2::Refresh
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
 - IFaxIncomingMessage2::Refresh
 - faxcomex/IFaxIncomingMessage2::Refresh
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
 - IFaxIncomingMessage2.Refresh
 - IFaxIncomingMessage2.Refresh
---

# IFaxIncomingMessage2::Refresh


## -description

Refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-save-vb">Save</a> method call are lost, except for the properties that are committed with the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-reassign-vb">IFaxIncomingMessage2::Reassign</a> method: <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">IFaxIncomingMessage2::Subject</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">IFaxIncomingMessage2::SenderName</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">IFaxIncomingMessage2::HasCoverPage</a>.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
