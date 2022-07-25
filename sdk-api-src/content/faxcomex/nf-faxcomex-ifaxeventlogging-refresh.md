---
UID: NF:faxcomex.IFaxEventLogging.Refresh
title: IFaxEventLogging::Refresh (faxcomex.h)
description: The IFaxEventLogging::Refresh method refreshes IFaxEventLogging interface information from the fax server.
helpviewer_keywords: ["IFaxEventLogging interface [Fax Service]","Refresh method","IFaxEventLogging.Refresh","IFaxEventLogging::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxEventLogging interface","_mfax_faxeventlogging.refresh","fax._mfax_faxeventlogging_cpp_mfax_faxeventlogging_refresh_cpp","fax._mfax_faxeventlogging_refresh","faxcomex/IFaxEventLogging::Refresh"]
old-location: fax\_mfax_faxeventlogging_cpp_mfax_faxeventlogging_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7ns8.htm
ms.date: 12/05/2018
ms.keywords: IFaxEventLogging interface [Fax Service],Refresh method, IFaxEventLogging.Refresh, IFaxEventLogging::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxEventLogging interface, _mfax_faxeventlogging.refresh, fax._mfax_faxeventlogging_cpp_mfax_faxeventlogging_refresh_cpp, fax._mfax_faxeventlogging_refresh, faxcomex/IFaxEventLogging::Refresh
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
 - IFaxEventLogging::Refresh
 - faxcomex/IFaxEventLogging::Refresh
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
 - IFaxEventLogging.Refresh
 - IFaxEventLogging.Refresh
---

# IFaxEventLogging::Refresh


## -description

The <b>IFaxEventLogging::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxeventlogging">IFaxEventLogging</a> interface information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the <a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging">FaxEventLogging</a> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging-save-vb">IFaxEventLogging::Save</a> method call are lost.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging">FaxEventLogging</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxeventlogging">IFaxEventLogging</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-logging-options">Visual Basic Example</a>
