---
UID: NF:faxcomex.IFaxReceiptOptions.Refresh
title: IFaxReceiptOptions::Refresh (faxcomex.h)
description: The IFaxReceiptOptions::Refresh method refreshes FaxReceiptOptions object information from the fax server. When the IFaxReceiptOptions::Refresh method is called, any configuration changes made after the last IFaxReceiptOptions::Save method call are lost.
helpviewer_keywords: ["IFaxReceiptOptions interface [Fax Service]","Refresh method","IFaxReceiptOptions.Refresh","IFaxReceiptOptions::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxReceiptOptions interface","_mfax_faxreceiptoptions.refresh","fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_refresh_cpp","fax._mfax_faxreceiptoptions_refresh","faxcomex/IFaxReceiptOptions::Refresh"]
old-location: fax\_mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xt4.htm
ms.date: 12/05/2018
ms.keywords: IFaxReceiptOptions interface [Fax Service],Refresh method, IFaxReceiptOptions.Refresh, IFaxReceiptOptions::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxReceiptOptions interface, _mfax_faxreceiptoptions.refresh, fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_refresh_cpp, fax._mfax_faxreceiptoptions_refresh, faxcomex/IFaxReceiptOptions::Refresh
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
 - IFaxReceiptOptions::Refresh
 - faxcomex/IFaxReceiptOptions::Refresh
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
 - IFaxReceiptOptions.Refresh
 - IFaxReceiptOptions.Refresh
---

# IFaxReceiptOptions::Refresh


## -description

The <b>IFaxReceiptOptions::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions">FaxReceiptOptions</a> object information from the fax server. When the <b>IFaxReceiptOptions::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions-save-vb">IFaxReceiptOptions::Save</a> method call are lost.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions">FaxReceiptOptions</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxreceiptoptions">IFaxReceiptOptions</a>
