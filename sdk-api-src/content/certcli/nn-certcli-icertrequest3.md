---
UID: NN:certcli.ICertRequest3
title: ICertRequest3 (certcli.h)
description: Provide communications between a client or intermediary application and Certificate Services. (ICertRequest3)
helpviewer_keywords: ["ICertRequest3","ICertRequest3 interface [Security]","ICertRequest3 interface [Security]","described","certcli/ICertRequest3","security.icertrequest3"]
old-location: security\icertrequest3.htm
tech.root: security
ms.assetid: 01de2ac0-4844-41a6-acef-e3e83b350393
ms.date: 12/05/2018
ms.keywords: ICertRequest3, ICertRequest3 interface [Security], ICertRequest3 interface [Security],described, certcli/ICertRequest3, security.icertrequest3
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ICertRequest3
 - certcli/ICertRequest3
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
 - ICertRequest3
---

# ICertRequest3 interface


## -description

The <b>ICertRequest3</b> interface is one of three interfaces that  provide communications between a client or intermediary application and <a href="/windows/desktop/SecGloss/c-gly">Certificate Services</a>.

Client and intermediary applications can call the  <b>ICertRequest3</b> methods to perform the following tasks:<ul>
<li>Submit a certificate request.</li>
<li>Retrieve the disposition, last status, and identifier of a request.</li>
<li>Retrieve the certificate issued for the request.</li>
<li>Retrieve pending certificates for previous requests.</li>
<li>Retrieve the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate for the Certificate Services server.</li>
<li>Retrieve the CA property value, display name, and any flags associated with the property.</li>
<li>Retrieve the cached response data returned by the server.</li>
<li>Retrieve error message text for an <b>HRESULT</b> error code.</li>
</ul>


<b>ICertRequest3</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertRequest3</b> interface. The type information for this interface is also in Certcli.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertRequest3</b> interface inherits from <a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>, <a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>, and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertRequest3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
