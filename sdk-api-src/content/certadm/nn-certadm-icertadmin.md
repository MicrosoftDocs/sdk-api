---
UID: NN:certadm.ICertAdmin
title: ICertAdmin (certadm.h)
description: Provides administration functionality for properly authorized clients.
helpviewer_keywords: ["ICertAdmin","ICertAdmin interface [Security]","ICertAdmin interface [Security]","described","_certsrv_icertadmin","certadm/ICertAdmin","security.icertadmin"]
old-location: security\icertadmin.htm
tech.root: security
ms.assetid: e906b69b-5574-4dd5-aa30-9c2a67972202
ms.date: 12/05/2018
ms.keywords: ICertAdmin, ICertAdmin interface [Security], ICertAdmin interface [Security],described, _certsrv_icertadmin, certadm/ICertAdmin, security.icertadmin
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin
 - certadm/ICertAdmin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin
---

# ICertAdmin interface


## -description

The <b>ICertAdmin</b> interface
			provides administration functionality for properly authorized clients.

The <b>ICertAdmin</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a certificate request.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
</ul>When you use the <b>ICertAdmin</b> interface, you have write-only access to request attributes and certificate extensions, but no direct access to other request and certificate properties.

<b>ICertAdmin</b> is defined in Certadm.h. When you create a program, however, use Certsrv.h as the include file. Certadm.dll, on the other hand, provides the implementation of the <b>ICertAdmin</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertAdmin</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertAdmin</b> also has these types of members:

