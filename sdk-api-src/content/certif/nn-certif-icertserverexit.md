---
UID: NN:certif.ICertServerExit
title: ICertServerExit (certif.h)
description: Exported by the server engine and is called by exit modules.
helpviewer_keywords: ["ICertServerExit","ICertServerExit interface [Security]","ICertServerExit interface [Security]","described","_certsrv_icertserverexit","certif/ICertServerExit","security.icertserverexit"]
old-location: security\icertserverexit.htm
tech.root: security
ms.assetid: 1554c09c-a7c1-44ad-9821-93c0913212fc
ms.date: 12/05/2018
ms.keywords: ICertServerExit, ICertServerExit interface [Security], ICertServerExit interface [Security],described, _certsrv_icertserverexit, certif/ICertServerExit, security.icertserverexit
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
 - ICertServerExit
 - certif/ICertServerExit
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
 - ICertServerExit
---

# ICertServerExit interface


## -description

The <b>ICertServerExit</b> interface is exported by the server engine and is called by exit modules.

<b>ICertServerExit</b> allows exit modules to get and enumerate elements of requests and certificates.

<b>ICertServerExit</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerExit</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertServerExit</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertServerExit</b> also has these types of members:

