---
UID: NF:faxcomex.IFaxAccountOutgoingArchive.Refresh
title: IFaxAccountOutgoingArchive::Refresh (faxcomex.h)
description: Refreshes FaxAccountOutgoingArchive object information for a particular fax account from the fax server.
helpviewer_keywords: ["IFaxAccountOutgoingArchive interface [Fax Service]","Refresh method","IFaxAccountOutgoingArchive.Refresh","IFaxAccountOutgoingArchive::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxAccountOutgoingArchive interface","_mfax_faxaccountoutgoingarchive.refresh","fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_refresh_cpp","fax._mfax_faxaccountoutgoingarchive_refresh","faxcomex/IFaxAccountOutgoingArchive::Refresh"]
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\refresh.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountOutgoingArchive interface [Fax Service],Refresh method, IFaxAccountOutgoingArchive.Refresh, IFaxAccountOutgoingArchive::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxAccountOutgoingArchive interface, _mfax_faxaccountoutgoingarchive.refresh, fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_refresh_cpp, fax._mfax_faxaccountoutgoingarchive_refresh, faxcomex/IFaxAccountOutgoingArchive::Refresh
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
 - IFaxAccountOutgoingArchive::Refresh
 - faxcomex/IFaxAccountOutgoingArchive::Refresh
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
 - IFaxAccountOutgoingArchive.Refresh
 - IFaxAccountOutgoingArchive.Refresh
---

# IFaxAccountOutgoingArchive::Refresh


## -description

Refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingarchive">FaxAccountOutgoingArchive</a> object information for a particular fax account from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingarchive">FaxAccountOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a>
