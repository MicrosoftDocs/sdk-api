---
UID: NN:certcli.ICertRequest
title: ICertRequest (certcli.h)
description: Provides communications between a client or intermediary application and Certificate services.
helpviewer_keywords: ["ICertRequest","ICertRequest interface [Security]","ICertRequest interface [Security]","described","_certsrv_icertrequest","certcli/ICertRequest","security.icertrequest"]
old-location: security\icertrequest.htm
tech.root: security
ms.assetid: 2f371aa6-492e-41ba-8455-66e9d5f5da44
ms.date: 12/05/2018
ms.keywords: ICertRequest, ICertRequest interface [Security], ICertRequest interface [Security],described, _certsrv_icertrequest, certcli/ICertRequest, security.icertrequest
req.header: certcli.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest
 - certcli/ICertRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest
---

# ICertRequest interface


## -description

The <b>ICertRequest</b> interface provides communications between a client or intermediary application and Certificate services.

Client and intermediary applications can call the  <b>ICertRequest</b> methods to perform the following tasks:<ul>
<li>Submit certificate request.</li>
<li>Retrieve the disposition, last status, and identifier of a request.</li>
<li>Retrieve the certificate issued for the request.</li>
<li>Retrieve pending certificates for previous requests.</li>
<li>Retrieve the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate for the Certificate Services server.</li>
</ul>


<b>ICertRequest</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertRequest</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertRequest</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertRequest</b> also has these types of members:

