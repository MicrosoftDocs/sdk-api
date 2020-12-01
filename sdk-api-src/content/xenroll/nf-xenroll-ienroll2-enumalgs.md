---
UID: NF:xenroll.IEnroll2.EnumAlgs
title: IEnroll2::EnumAlgs (xenroll.h)
description: Retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current cryptographic service provider (CSP).
helpviewer_keywords: ["EnumAlgs","EnumAlgs method [Security]","EnumAlgs method [Security]","IEnroll2 interface","IEnroll2 interface [Security]","EnumAlgs method","IEnroll2.EnumAlgs","IEnroll2::EnumAlgs","security.ienroll4_enumalgs","xenroll/IEnroll2::EnumAlgs"]
old-location: security\ienroll4_enumalgs.htm
tech.root: security
ms.assetid: a40d85d0-fd02-4e0a-af7d-dfefe02f4e2a
ms.date: 12/05/2018
ms.keywords: EnumAlgs, EnumAlgs method [Security], EnumAlgs method [Security],IEnroll2 interface, IEnroll2 interface [Security],EnumAlgs method, IEnroll2.EnumAlgs, IEnroll2::EnumAlgs, security.ienroll4_enumalgs, xenroll/IEnroll2::EnumAlgs
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
 - IEnroll2::EnumAlgs
 - xenroll/IEnroll2::EnumAlgs
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
 - IEnroll2.EnumAlgs
---

# IEnroll2::EnumAlgs


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnumAlgs</b> method retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).  This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

## -parameters

### -param dwIndex [in]

Specifies the ordinal position of the algorithm whose ID will be retrieved. Specify zero for the first algorithm.

### -param algClass [in]

A cryptographic algorithm class. The IDs returned by this method will be in the specified class. Specify one of the following:

<ul>
<li>ALG_CLASS_HASH</li>
<li>ALG_CLASS_KEY_EXCHANGE</li>
<li>ALG_CLASS_MSG_ENCRYPT</li>
<li>ALG_CLASS_DATA_ENCRYPT</li>
<li>ALG_CLASS_SIGNATURE</li>
</ul>

### -param pdwAlgID [out]

A pointer to LONG which receives a cryptographic algorithm ID which is supported by the current CSP.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. When there are no more algorithms to enumerate, the value ERROR_NO_MORE_ITEMS is returned.

## -remarks

For algorithm ID and class constants used by this method, see Wincrypt.h.

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>