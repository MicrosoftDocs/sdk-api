---
UID: NN:faxcomex.IFaxSecurity
title: IFaxSecurity (faxcomex.h)
description: The IFaxSecurity configuration object is used by a fax client application to configure the security on a fax server, and permits the calling application to set and retrieve a security descriptor for the fax server.
helpviewer_keywords: ["IFaxSecurity","IFaxSecurity interface [Fax Service]","IFaxSecurity interface [Fax Service]","described","_mfax_faxsecurity_cpp","fax._mfax_faxsecurity_cpp","faxcomex/IFaxSecurity"]
old-location: fax\_mfax_faxsecurity_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_63cp_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity, IFaxSecurity interface [Fax Service], IFaxSecurity interface [Fax Service],described, _mfax_faxsecurity_cpp, fax._mfax_faxsecurity_cpp, faxcomex/IFaxSecurity
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
 - IFaxSecurity
 - faxcomex/IFaxSecurity
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
 - IFaxSecurity
---

# IFaxSecurity interface


## -description

The <b>IFaxSecurity</b> configuration object is used by a fax client application to configure the security on a fax server, and permits the calling application to set and retrieve a security descriptor for the fax server.

## -inheritance

The <b>IFaxSecurity</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxSecurity</b> also has these types of members:

## -remarks

Only an administrator with permissions can configure the security of the fax server. For more information, see <a href="/windows/desktop/FWP/access-control">Access Control</a>.

A default implementation of <b>IFaxSecurity</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a> object.
