---
UID: NF:xenroll.IEnroll.freeRequestInfoBlob
title: IEnroll::freeRequestInfoBlob (xenroll.h)
description: The freeRequestInfoBlob method deletes a certificate context. This method was first defined in the IEnroll interface.
helpviewer_keywords: ["IEnroll interface [Security]","freeRequestInfoBlob method","IEnroll.freeRequestInfoBlob","IEnroll::freeRequestInfoBlob","freeRequestInfoBlob","freeRequestInfoBlob method [Security]","freeRequestInfoBlob method [Security]","IEnroll interface","security.ienroll4_freerequestinfoblob","xenroll/IEnroll::freeRequestInfoBlob"]
old-location: security\ienroll4_freerequestinfoblob.htm
tech.root: security
ms.assetid: 7c89de98-51b6-44c2-acd2-879d1d4e7f29
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],freeRequestInfoBlob method, IEnroll.freeRequestInfoBlob, IEnroll::freeRequestInfoBlob, freeRequestInfoBlob, freeRequestInfoBlob method [Security], freeRequestInfoBlob method [Security],IEnroll interface, security.ienroll4_freerequestinfoblob, xenroll/IEnroll::freeRequestInfoBlob
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
 - IEnroll::freeRequestInfoBlob
 - xenroll/IEnroll::freeRequestInfoBlob
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
 - IEnroll.freeRequestInfoBlob
---

# IEnroll::freeRequestInfoBlob


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>freeRequestInfoBlob</b> method deletes a certificate context. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param pkcs7OrPkcs10 [in]

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that specifies the session information whose context is being deleted.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>