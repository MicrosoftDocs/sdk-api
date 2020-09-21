---
UID: NF:certif.ICertServerExit.SetContext
title: ICertServerExit::SetContext (certif.h)
description: Causes the current instantiation of the interface to operate on the request referenced by Context.
helpviewer_keywords: ["CCertServerExit object [Security]","SetContext method","ICertServerExit interface [Security]","SetContext method","ICertServerExit.SetContext","ICertServerExit::SetContext","SetContext","SetContext method [Security]","SetContext method [Security]","CCertServerExit object","SetContext method [Security]","ICertServerExit interface","_certsrv_icertserverexit_setcontext","certif/ICertServerExit::SetContext","security.icertserverexit_setcontext"]
old-location: security\icertserverexit_setcontext.htm
tech.root: security
ms.assetid: 8d317114-17bd-4b22-8e37-99db72740538
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],SetContext method, ICertServerExit interface [Security],SetContext method, ICertServerExit.SetContext, ICertServerExit::SetContext, SetContext, SetContext method [Security], SetContext method [Security],CCertServerExit object, SetContext method [Security],ICertServerExit interface, _certsrv_icertserverexit_setcontext, certif/ICertServerExit::SetContext, security.icertserverexit_setcontext
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
 - ICertServerExit::SetContext
 - certif/ICertServerExit::SetContext
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
 - ICertServerExit.SetContext
 - CCertServerExit.SetContext
---

# ICertServerExit::SetContext


## -description

The <b>SetContext</b> method causes the current instantiation of the interface to operate on the request referenced by <i>Context</i>.

This must be identical to a value given by the <i>Context</i> parameter in 
<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-notify">ICertExit::Notify</a>. This method must be called before calling any of the other 
<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a> methods, in order that the interface reference a valid request.

## -parameters

### -param Context [in]

Specifies the request and associated certificate under construction.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-notify">ICertExit::Notify</a>



<a href="/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a>



<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>