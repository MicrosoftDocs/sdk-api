---
UID: NF:faxcomex.IFaxIncomingArchive.Refresh
title: IFaxIncomingArchive::Refresh (faxcomex.h)
description: The Refresh method refreshes FaxIncomingArchive object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
helpviewer_keywords: ["IFaxIncomingArchive interface [Fax Service]","Refresh method","IFaxIncomingArchive.Refresh","IFaxIncomingArchive::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxIncomingArchive interface","_mfax_faxincomingarchive.refresh","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_refresh_cpp","fax._mfax_faxincomingarchive_refresh","faxcomex/IFaxIncomingArchive::Refresh"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_827c.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],Refresh method, IFaxIncomingArchive.Refresh, IFaxIncomingArchive::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.refresh, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_refresh_cpp, fax._mfax_faxincomingarchive_refresh, faxcomex/IFaxIncomingArchive::Refresh
f1_keywords:
- faxcomex/IFaxIncomingArchive.Refresh
dev_langs:
- c++
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
- IFaxIncomingArchive.Refresh
- IFaxIncomingArchive.Refresh
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingArchive::Refresh


## -description


The <b>Refresh</b> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-save-vb">Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>
 

 

