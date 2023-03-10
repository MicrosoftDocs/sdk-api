---
UID: NN:certif.ICertServerPolicy
title: ICertServerPolicy (certif.h)
description: Allows the policy module to communicate with Certificate Services.
helpviewer_keywords: ["ICertServerPolicy","ICertServerPolicy interface [Security]","ICertServerPolicy interface [Security]","described","_certsrv_icertserverpolicy","certif/ICertServerPolicy","security.icertserverpolicy"]
old-location: security\icertserverpolicy.htm
tech.root: security
ms.assetid: 7d16161e-9827-46a0-9989-30ebca792bb1
ms.date: 12/05/2018
ms.keywords: ICertServerPolicy, ICertServerPolicy interface [Security], ICertServerPolicy interface [Security],described, _certsrv_icertserverpolicy, certif/ICertServerPolicy, security.icertserverpolicy
req.header: certif.h
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
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertServerPolicy
 - certif/ICertServerPolicy
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
 - ICertServerPolicy
---

# ICertServerPolicy interface


## -description

The <b>ICertServerPolicy</b> interface allows the policy module to communicate with Certificate Services.
<div class="alert"><b>Note</b>  Certificate Services communicates with the policy module through the <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a> interface.</div><div> </div>The <b>ICertServerPolicy</b> interface is exported by the server engine and is called by the policy module to perform the following tasks:<ul>
<li>Specify which certificate request  is used as the current context for subsequent operations.</li>
<li>Enumerate and  retrieve the extensions (including extension flags) of a certificate request, and set the extensions of the issued certificate.</li>
<li>Enumerate and retrieve request attributes.</li>
<li>Retrieve certificate request properties.</li>
<li>Retrieve and set certificate properties.</li>
</ul>


From the time the 
<a href="/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a> method is called until it returns, the unresolved request and certificate under construction can be accessed through a Context data object. Because the policy module can add to or override request properties by calling 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcertificateproperty">ICertServerPolicy::SetCertificateProperty</a>, certificate properties can differ from request properties.

<b>ICertServerPolicy</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerPolicy</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertServerPolicy</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertServerPolicy</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-resubmitrequest">ICertAdmin::ResubmitRequest</a>



<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-setrequestattributes">ICertAdmin::SetRequestAttributes</a>



<a href="/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest::Submit</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
