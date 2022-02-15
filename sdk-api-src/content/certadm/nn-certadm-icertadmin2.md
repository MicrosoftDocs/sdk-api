---
UID: NN:certadm.ICertAdmin2
title: ICertAdmin2 (certadm.h)
description: Provide administration functionality for properly authorized clients.
helpviewer_keywords: ["ICertAdmin2","ICertAdmin2 interface [Security]","ICertAdmin2 interface [Security]","described","_certsrv_icertadmin2","certadm/ICertAdmin2","security.icertadmin2"]
old-location: security\icertadmin2.htm
tech.root: security
ms.assetid: df40b6ac-825d-4e8d-a80b-6e57a4e740a2
ms.date: 12/05/2018
ms.keywords: ICertAdmin2, ICertAdmin2 interface [Security], ICertAdmin2 interface [Security],described, _certsrv_icertadmin2, certadm/ICertAdmin2, security.icertadmin2
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
 - ICertAdmin2
 - certadm/ICertAdmin2
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
 - ICertAdmin2
---

# ICertAdmin2 interface


## -description

The <b>ICertAdmin2</b> interface
			is one of two interfaces that provide administration functionality for properly authorized clients.

The <b>ICertAdmin2</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
<li>Get an archived key.</li>
<li>Get a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) display name, property, or property flag.</li>
<li>Publish one or several CRLs.</li>
<li>Get or set configuration information.</li>
<li>Determine which roles are set.</li>
<li>Import a certificate or key.</li>
</ul>Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertAdmin2</b> interface inherits from <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertAdmin2</b> also has these types of members:

