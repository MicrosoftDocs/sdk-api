---
UID: NF:faxcomex.IFaxAccountIncomingArchive.Refresh
title: IFaxAccountIncomingArchive::Refresh (faxcomex.h)
description: Refreshes FaxAccountIncomingArchive object information for a particular fax account from the fax server.
helpviewer_keywords: ["IFaxAccountIncomingArchive interface [Fax Service]","Refresh method","IFaxAccountIncomingArchive.Refresh","IFaxAccountIncomingArchive::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxAccountIncomingArchive interface","_mfax_faxaccountincomingarchive.refresh","fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_refresh_cpp","fax._mfax_faxaccountincomingarchive_refresh","faxcomex/IFaxAccountIncomingArchive::Refresh"]
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\refresh.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountIncomingArchive interface [Fax Service],Refresh method, IFaxAccountIncomingArchive.Refresh, IFaxAccountIncomingArchive::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxAccountIncomingArchive interface, _mfax_faxaccountincomingarchive.refresh, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_refresh_cpp, fax._mfax_faxaccountincomingarchive_refresh, faxcomex/IFaxAccountIncomingArchive::Refresh
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
 - IFaxAccountIncomingArchive::Refresh
 - faxcomex/IFaxAccountIncomingArchive::Refresh
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
 - IFaxAccountIncomingArchive.Refresh
 - IFaxAccountIncomingArchive.Refresh
---

# IFaxAccountIncomingArchive::Refresh


## -description

Refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive">FaxAccountIncomingArchive</a> object information for a particular fax account from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive">FaxAccountIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingarchive">IFaxAccountIncomingArchive</a>
