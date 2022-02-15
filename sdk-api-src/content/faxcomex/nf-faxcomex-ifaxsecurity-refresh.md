---
UID: NF:faxcomex.IFaxSecurity.Refresh
title: IFaxSecurity::Refresh (faxcomex.h)
description: The IFaxSecurity::Refresh method refreshes FaxSecurity object information from the fax server.
helpviewer_keywords: ["IFaxSecurity interface [Fax Service]","Refresh method","IFaxSecurity.Refresh","IFaxSecurity::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxSecurity interface","_mfax_faxsecurity.refresh","fax._mfax_faxsecurity_cpp_mfax_faxsecurity_refresh_cpp","fax._mfax_faxsecurity_refresh","faxcomex/IFaxSecurity::Refresh"]
old-location: fax\_mfax_faxsecurity_cpp_mfax_faxsecurity_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9xrc.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity interface [Fax Service],Refresh method, IFaxSecurity.Refresh, IFaxSecurity::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxSecurity interface, _mfax_faxsecurity.refresh, fax._mfax_faxsecurity_cpp_mfax_faxsecurity_refresh_cpp, fax._mfax_faxsecurity_refresh, faxcomex/IFaxSecurity::Refresh
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
 - IFaxSecurity::Refresh
 - faxcomex/IFaxSecurity::Refresh
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
 - IFaxSecurity.Refresh
 - IFaxSecurity.Refresh
---

# IFaxSecurity::Refresh


## -description

The <b>IFaxSecurity::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a> object information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the <b>IFaxSecurity::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity-save-vb">IFaxSecurity::Save</a> method call are lost.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity">IFaxSecurity</a>
