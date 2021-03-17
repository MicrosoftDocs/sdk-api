---
UID: NF:xenroll.ICEnroll4.removePendingRequest
title: ICEnroll4::removePendingRequest (xenroll.h)
description: Removes a pending request from the client's request store. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","removePendingRequest method","ICEnroll4 interface [Security]","removePendingRequest method","ICEnroll4.removePendingRequest","ICEnroll4::removePendingRequest","_xen_icenroll4_removependingrequest","removePendingRequest","removePendingRequest method [Security]","removePendingRequest method [Security]","CEnroll object","removePendingRequest method [Security]","ICEnroll4 interface","security.icenroll4_removependingrequest","xenroll/ICEnroll4::removePendingRequest"]
old-location: security\icenroll4_removependingrequest.htm
tech.root: security
ms.assetid: 22ddd7f8-b2c0-4b9a-a2b3-c2cb470d0502
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],removePendingRequest method, ICEnroll4 interface [Security],removePendingRequest method, ICEnroll4.removePendingRequest, ICEnroll4::removePendingRequest, _xen_icenroll4_removependingrequest, removePendingRequest, removePendingRequest method [Security], removePendingRequest method [Security],CEnroll object, removePendingRequest method [Security],ICEnroll4 interface, security.icenroll4_removependingrequest, xenroll/ICEnroll4::removePendingRequest
req.header: xenroll.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll4::removePendingRequest
 - xenroll/ICEnroll4::removePendingRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.removePendingRequest
 - CEnroll.removePendingRequest
---

# ICEnroll4::removePendingRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>removePendingRequest</b> method removes a pending request from the client's request store. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param strThumbprint [in]

The thumbprint, or <a href="/windows/desktop/SecGloss/h-gly">hash</a>, of the certificate data.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.