---
UID: NF:faxcomex.IFaxActivityLogging.Refresh
title: IFaxActivityLogging::Refresh (faxcomex.h)
description: The IFaxActivityLogging::Refresh method refreshes FaxActivityLogging object information from the fax server.
helpviewer_keywords: ["IFaxActivityLogging interface [Fax Service]","Refresh method","IFaxActivityLogging.Refresh","IFaxActivityLogging::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxActivityLogging interface","_mfax_faxactivitylogging.refresh","fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_refresh_cpp","fax._mfax_faxactivitylogging_refresh","faxcomex/IFaxActivityLogging::Refresh"]
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1gko.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],Refresh method, IFaxActivityLogging.Refresh, IFaxActivityLogging::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.refresh, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_refresh_cpp, fax._mfax_faxactivitylogging_refresh, faxcomex/IFaxActivityLogging::Refresh
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
 - IFaxActivityLogging::Refresh
 - faxcomex/IFaxActivityLogging::Refresh
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
 - IFaxActivityLogging.Refresh
 - IFaxActivityLogging.Refresh
---

# IFaxActivityLogging::Refresh


## -description

The <b>IFaxActivityLogging::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> object information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the <b>IFaxActivityLogging::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-save-vb">IFaxActivityLogging::Save</a> method call are lost.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivitylogging">IFaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-logging-options">Visual Basic Example</a>
