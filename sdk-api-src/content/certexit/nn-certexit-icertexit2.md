---
UID: NN:certexit.ICertExit2
title: ICertExit2 (certexit.h)
description: Provide communications between the Certificate Services server and an exit module.
helpviewer_keywords: ["ICertExit2","ICertExit2 interface [Security]","ICertExit2 interface [Security]","described","_certsrv_icertexit2","certexit/ICertExit2","security.icertexit2"]
old-location: security\icertexit2.htm
tech.root: security
ms.assetid: a9d66aeb-b596-4d50-9c07-b760cdf4f8c0
ms.date: 12/05/2018
ms.keywords: ICertExit2, ICertExit2 interface [Security], ICertExit2 interface [Security],described, _certsrv_icertexit2, certexit/ICertExit2, security.icertexit2
req.header: certexit.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertExit2
 - certexit/ICertExit2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certexit.h
api_name:
 - ICertExit2
---

# ICertExit2 interface


## -description

The <b>ICertExit2</b> interface is one of two interfaces that   provide communications between  the Certificate Services server and an exit module.
<div class="alert"><b>Note</b>  The exit module can communicate with the Certificate Services server by using the <a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a> interface.</div><div> </div>The Certificate Services server calls the <b>ICertExit2</b> methods to perform the following tasks:<ul>
<li>Initialize the Certificate Services server.</li>
<li>Notify the exit module of an event such as certificate issuance, <a href="/windows/desktop/SecGloss/c-gly">CRL</a> issuance, or server shutdown, has occurred.</li>
<li>Retrieve a description of the exit module.</li>
<li>Retrieve the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface implemented by the exit module. The methods of this interface allows the Certificate Services server to configure the exit module as well as set and retrieve the exit module properties.</li>
</ul>


<b>ICertExit2</b> is defined in Certexit.h. When you create your program, however, use Certsrv.h as the include file.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertExit2</b> interface inherits from <a href="/windows/desktop/api/certexit/nn-certexit-icertexit">ICertExit</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertExit2</b> also has these types of members:

