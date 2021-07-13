---
UID: NF:certif.ICertServerExit.EnumerateExtensionsClose
title: ICertServerExit::EnumerateExtensionsClose (certif.h)
description: Frees any resources connected with extension enumeration.
helpviewer_keywords: ["CCertServerExit object [Security]","EnumerateExtensionsClose method","EnumerateExtensionsClose","EnumerateExtensionsClose method [Security]","EnumerateExtensionsClose method [Security]","CCertServerExit object","EnumerateExtensionsClose method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","EnumerateExtensionsClose method","ICertServerExit.EnumerateExtensionsClose","ICertServerExit::EnumerateExtensionsClose","_certsrv_icertserverexit_enumerateextensionsclose","certif/ICertServerExit::EnumerateExtensionsClose","security.icertserverexit_enumerateextensionsclose"]
old-location: security\icertserverexit_enumerateextensionsclose.htm
tech.root: security
ms.assetid: 769235cd-d5ef-458b-a04b-88f9f831ce3f
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],EnumerateExtensionsClose method, EnumerateExtensionsClose, EnumerateExtensionsClose method [Security], EnumerateExtensionsClose method [Security],CCertServerExit object, EnumerateExtensionsClose method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateExtensionsClose method, ICertServerExit.EnumerateExtensionsClose, ICertServerExit::EnumerateExtensionsClose, _certsrv_icertserverexit_enumerateextensionsclose, certif/ICertServerExit::EnumerateExtensionsClose, security.icertserverexit_enumerateextensionsclose
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
 - ICertServerExit::EnumerateExtensionsClose
 - certif/ICertServerExit::EnumerateExtensionsClose
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
 - ICertServerExit.EnumerateExtensionsClose
 - CCertServerExit.EnumerateExtensionsClose
---

# ICertServerExit::EnumerateExtensionsClose


## -description

The <b>EnumerateExtensionsClose</b>  method frees any resources connected with extension enumeration.

All applications that use <a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionssetup">ICertServerExit::EnumerateExtensionsSetup</a> and <a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensions">ICertServerExit::EnumerateExtensions</a> should call <b>EnumerateExtensionsClose</b> when finished enumerating.



## -see-also

<b>CCertServerExit</b>



<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>
