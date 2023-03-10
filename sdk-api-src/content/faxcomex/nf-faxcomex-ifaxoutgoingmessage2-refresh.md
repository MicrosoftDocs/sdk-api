---
UID: NF:faxcomex.IFaxOutgoingMessage2.Refresh
title: IFaxOutgoingMessage2::Refresh (faxcomex.h)
description: Refreshes FaxOutgoingMessage object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
helpviewer_keywords: ["IFaxOutgoingMessage2 interface [Fax Service]","Refresh method","IFaxOutgoingMessage2.Refresh","IFaxOutgoingMessage2::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxOutgoingMessage2 interface","_mfax_faxoutgoingmessage.refresh","fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp","fax._mfax_faxoutgoingmessage_refresh","faxcomex/IFaxOutgoingMessage2::Refresh"]
old-location: fax\_mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\refresh.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessage2 interface [Fax Service],Refresh method, IFaxOutgoingMessage2.Refresh, IFaxOutgoingMessage2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingMessage2 interface, _mfax_faxoutgoingmessage.refresh, fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp, fax._mfax_faxoutgoingmessage_refresh, faxcomex/IFaxOutgoingMessage2::Refresh
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
 - IFaxOutgoingMessage2::Refresh
 - faxcomex/IFaxOutgoingMessage2::Refresh
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
 - IFaxOutgoingMessage2.Refresh
 - IFaxOutgoingMessage2.Refresh
---

# IFaxOutgoingMessage2::Refresh


## -description

Refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-save-vb">Save</a> method call are lost.


<div class="alert"><b>Note</b>  This method is supported only on Windows Vista and later.</div><div> </div>



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage2">IFaxOutgoingMessage2</a>
