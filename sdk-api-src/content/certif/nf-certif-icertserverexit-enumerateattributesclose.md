---
UID: NF:certif.ICertServerExit.EnumerateAttributesClose
title: ICertServerExit::EnumerateAttributesClose (certif.h)
description: Frees any resources connected with attribute enumeration.
helpviewer_keywords: ["CCertServerExit object [Security]","EnumerateAttributesClose method","EnumerateAttributesClose","EnumerateAttributesClose method [Security]","EnumerateAttributesClose method [Security]","CCertServerExit object","EnumerateAttributesClose method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","EnumerateAttributesClose method","ICertServerExit.EnumerateAttributesClose","ICertServerExit::EnumerateAttributesClose","_certsrv_icertserverexit_enumerateattributesclose","certif/ICertServerExit::EnumerateAttributesClose","security.icertserverexit_enumerateattributesclose"]
old-location: security\icertserverexit_enumerateattributesclose.htm
tech.root: security
ms.assetid: 6ac7afbb-49c6-45b3-a27e-5ba995684848
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],EnumerateAttributesClose method, EnumerateAttributesClose, EnumerateAttributesClose method [Security], EnumerateAttributesClose method [Security],CCertServerExit object, EnumerateAttributesClose method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateAttributesClose method, ICertServerExit.EnumerateAttributesClose, ICertServerExit::EnumerateAttributesClose, _certsrv_icertserverexit_enumerateattributesclose, certif/ICertServerExit::EnumerateAttributesClose, security.icertserverexit_enumerateattributesclose
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
 - ICertServerExit::EnumerateAttributesClose
 - certif/ICertServerExit::EnumerateAttributesClose
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
 - ICertServerExit.EnumerateAttributesClose
 - CCertServerExit.EnumerateAttributesClose
---

# ICertServerExit::EnumerateAttributesClose


## -description

The <b>EnumerateAttributesClose</b> method frees any resources connected with <a href="/windows/desktop/SecGloss/a-gly">attribute</a> enumeration.

All applications that use 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributessetup">ICertServerExit::EnumerateAttributesSetup</a> or 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributes">ICertServerExit::EnumerateAttributes</a> should call <b>EnumerateAttributesClose</b> when finished enumerating.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributes">ICertServerExit::EnumerateAttributes</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributessetup">ICertServerExit::EnumerateAttributesSetup</a>
