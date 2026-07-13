---
UID: NF:faxcomex.IFaxOutgoingArchive.Refresh
title: IFaxOutgoingArchive::Refresh (faxcomex.h)
description: The IFaxOutgoingArchive::Refresh method refreshes FaxOutgoingArchive object information from the fax server.
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","Refresh method","IFaxOutgoingArchive.Refresh","IFaxOutgoingArchive::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.refresh","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_refresh_cpp","fax._mfax_faxoutgoingarchive_refresh","faxcomex/IFaxOutgoingArchive::Refresh"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6hm0.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],Refresh method, IFaxOutgoingArchive.Refresh, IFaxOutgoingArchive::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.refresh, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_refresh_cpp, fax._mfax_faxoutgoingarchive_refresh, faxcomex/IFaxOutgoingArchive::Refresh
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
 - IFaxOutgoingArchive::Refresh
 - faxcomex/IFaxOutgoingArchive::Refresh
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
 - IFaxOutgoingArchive.Refresh
 - IFaxOutgoingArchive.Refresh
---

# IFaxOutgoingArchive::Refresh


## -description

The <b>IFaxOutgoingArchive::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a> object information from the fax server. When the <b>IFaxOutgoingArchive::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive-save-vb">IFaxOutgoingArchive::Save</a> method call are lost.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>
