---
UID: NF:faxcomex.IFaxActivity.Refresh
title: IFaxActivity::Refresh (faxcomex.h)
description: The IFaxActivity::Refresh method refreshes FaxActivity information from the fax server.
helpviewer_keywords: ["IFaxActivity interface [Fax Service]","Refresh method","IFaxActivity.Refresh","IFaxActivity::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxActivity interface","_mfax_faxactivity.refresh","fax._mfax_faxactivity_cpp_mfax_faxactivity_refresh_cpp","fax._mfax_faxactivity_refresh","faxcomex/IFaxActivity::Refresh"]
old-location: fax\_mfax_faxactivity_cpp_mfax_faxactivity_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4krs.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivity interface [Fax Service],Refresh method, IFaxActivity.Refresh, IFaxActivity::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxActivity interface, _mfax_faxactivity.refresh, fax._mfax_faxactivity_cpp_mfax_faxactivity_refresh_cpp, fax._mfax_faxactivity_refresh, faxcomex/IFaxActivity::Refresh
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
 - IFaxActivity::Refresh
 - faxcomex/IFaxActivity::Refresh
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
 - IFaxActivity.Refresh
 - IFaxActivity.Refresh
---

# IFaxActivity::Refresh


## -description

The <b>IFaxActivity::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivity">FaxActivity</a> information from the fax server.

The <b>IFaxActivity::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivity">IFaxActivity</a> information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxactivity">FaxActivity</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivity">IFaxActivity</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-monitoring-fax-activity">Visual Basic Example</a>
