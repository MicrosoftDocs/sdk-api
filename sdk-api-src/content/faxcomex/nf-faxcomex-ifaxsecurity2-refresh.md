---
UID: NF:faxcomex.IFaxSecurity2.Refresh
title: IFaxSecurity2::Refresh (faxcomex.h)
description: Refreshes FaxSecurity2 object information from the fax server.
helpviewer_keywords: ["IFaxSecurity2 interface [Fax Service]","Refresh method","IFaxSecurity2.Refresh","IFaxSecurity2::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxSecurity2 interface","_mfax_faxsecurity2.refresh","fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_refresh_cpp","fax._mfax_faxsecurity2_refresh","faxcomex/IFaxSecurity2::Refresh"]
old-location: fax\_mfax_faxsecurity2_cpp_mfax_faxsecurity2_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\refresh.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity2 interface [Fax Service],Refresh method, IFaxSecurity2.Refresh, IFaxSecurity2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxSecurity2 interface, _mfax_faxsecurity2.refresh, fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_refresh_cpp, fax._mfax_faxsecurity2_refresh, faxcomex/IFaxSecurity2::Refresh
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
 - IFaxSecurity2::Refresh
 - faxcomex/IFaxSecurity2::Refresh
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
 - IFaxSecurity2.Refresh
 - IFaxSecurity2.Refresh
---

# IFaxSecurity2::Refresh


## -description

Refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a> object information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the <b>IFaxSecurity2::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-save-vb">IFaxSecurity2::Save</a> method call are lost.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity2">IFaxSecurity2</a>
