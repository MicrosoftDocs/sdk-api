---
UID: NF:xenroll.IEnroll2.GetSupportedKeySpec
title: IEnroll2::GetSupportedKeySpec (xenroll.h)
description: Retrieves information regarding the current cryptographic service provider (CSP) support for signature and/or exchange operations.
helpviewer_keywords: ["GetSupportedKeySpec","GetSupportedKeySpec method [Security]","GetSupportedKeySpec method [Security]","IEnroll2 interface","IEnroll2 interface [Security]","GetSupportedKeySpec method","IEnroll2.GetSupportedKeySpec","IEnroll2::GetSupportedKeySpec","security.ienroll4_getsupportedkeyspec","xenroll/IEnroll2::GetSupportedKeySpec"]
old-location: security\ienroll4_getsupportedkeyspec.htm
tech.root: security
ms.assetid: 8f7ace8e-0102-4c89-9d8a-e252ad60bb96
ms.date: 12/05/2018
ms.keywords: GetSupportedKeySpec, GetSupportedKeySpec method [Security], GetSupportedKeySpec method [Security],IEnroll2 interface, IEnroll2 interface [Security],GetSupportedKeySpec method, IEnroll2.GetSupportedKeySpec, IEnroll2::GetSupportedKeySpec, security.ienroll4_getsupportedkeyspec, xenroll/IEnroll2::GetSupportedKeySpec
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
 - IEnroll2::GetSupportedKeySpec
 - xenroll/IEnroll2::GetSupportedKeySpec
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
 - IEnroll2.GetSupportedKeySpec
---

# IEnroll2::GetSupportedKeySpec


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetSupportedKeySpec</b> method retrieves information regarding the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) support for signature and/or exchange operations. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

The values retrieved by this method are dependent upon the current CSP.

## -parameters

### -param pdwKeySpec [out]

A pointer to a <b>LONG</b> that receives a bit flag indicating whether the current CSP supports <a href="/windows/desktop/SecGloss/e-gly">exchange</a> and/or <a href="/windows/desktop/SecGloss/s-gly">signature keys</a>.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. If a CSP does not support this method, an error is returned.

## -remarks

Call this method to determine whether the current CSP supports exchange keys, signature keys, or both. The <i>pdwKeySpec</i> parameter will contain one or more of the following constants (defined in Wincrypt.h):

<ul>
<li>AT_KEYEXCHANGE</li>
<li>AT_SIGNATURE.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>