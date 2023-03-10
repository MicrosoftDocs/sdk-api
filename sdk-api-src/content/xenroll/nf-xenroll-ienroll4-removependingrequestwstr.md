---
UID: NF:xenroll.IEnroll4.removePendingRequestWStr
title: IEnroll4::removePendingRequestWStr (xenroll.h)
description: Removes a pending request from the client's request store.
helpviewer_keywords: ["IEnroll4 interface [Security]","removePendingRequestWStr method","IEnroll4.removePendingRequestWStr","IEnroll4::removePendingRequestWStr","removePendingRequestWStr","removePendingRequestWStr method [Security]","removePendingRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_removependingrequestwstr","xenroll/IEnroll4::removePendingRequestWStr"]
old-location: security\ienroll4_removependingrequestwstr.htm
tech.root: security
ms.assetid: 0e00fad2-dc06-421d-9a8c-27c5a951466c
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],removePendingRequestWStr method, IEnroll4.removePendingRequestWStr, IEnroll4::removePendingRequestWStr, removePendingRequestWStr, removePendingRequestWStr method [Security], removePendingRequestWStr method [Security],IEnroll4 interface, security.ienroll4_removependingrequestwstr, xenroll/IEnroll4::removePendingRequestWStr
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
 - IEnroll4::removePendingRequestWStr
 - xenroll/IEnroll4::removePendingRequestWStr
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
 - IEnroll4.removePendingRequestWStr
---

# IEnroll4::removePendingRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>removePendingRequestWStr</b> method removes a pending request from the client's request store.  This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param thumbPrintBlob [in]

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the thumbprint, or <a href="/windows/desktop/SecGloss/h-gly">hash</a>, of the certificate data.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>