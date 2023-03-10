---
UID: NN:faxcomex.IFaxSecurity2
title: IFaxSecurity2 (faxcomex.h)
description: Used by a fax client application to configure the security on a fax server; also permits the calling application to set and retrieve a security descriptor for the fax server.
helpviewer_keywords: ["IFaxSecurity2","IFaxSecurity2 interface [Fax Service]","IFaxSecurity2 interface [Fax Service]","described","_mfax_faxsecurity2_cpp","fax._mfax_faxsecurity2_cpp","faxcomex/IFaxSecurity2"]
old-location: fax\_mfax_faxsecurity2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\faxinto_z_ifaxsecurity2.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity2, IFaxSecurity2 interface [Fax Service], IFaxSecurity2 interface [Fax Service],described, _mfax_faxsecurity2_cpp, fax._mfax_faxsecurity2_cpp, faxcomex/IFaxSecurity2
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
 - IFaxSecurity2
 - faxcomex/IFaxSecurity2
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
 - IFaxSecurity2
---

# IFaxSecurity2 interface


## -description

Used by a fax client application to configure the security on a fax server; also permits the calling application to set and retrieve a security descriptor for the fax server.

## -inheritance

The <b>IFaxSecurity2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxSecurity2</b> also has these types of members:

## -remarks

This interface is supported only on Windows Vista or later. For earlier versions of Windows use <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity">IFaxSecurity</a>.

Only an administrator with permissions can configure the security of the fax server. For more information, see <a href="/windows/desktop/FWP/access-control">Access Control</a>.

A default implementation is provided as <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a>.
