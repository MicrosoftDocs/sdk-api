---
UID: NF:xenroll.IEnroll2.GetAlgNameWStr
title: IEnroll2::GetAlgNameWStr (xenroll.h)
description: Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current cryptographic service provider (CSP).
helpviewer_keywords: ["GetAlgNameWStr","GetAlgNameWStr method [Security]","GetAlgNameWStr method [Security]","IEnroll2 interface","IEnroll2 interface [Security]","GetAlgNameWStr method","IEnroll2.GetAlgNameWStr","IEnroll2::GetAlgNameWStr","security.ienroll4_getalgnamewstr","xenroll/IEnroll2::GetAlgNameWStr"]
old-location: security\ienroll4_getalgnamewstr.htm
tech.root: security
ms.assetid: 2d628d26-a081-49a2-8fc9-88f014d24a4e
ms.date: 12/05/2018
ms.keywords: GetAlgNameWStr, GetAlgNameWStr method [Security], GetAlgNameWStr method [Security],IEnroll2 interface, IEnroll2 interface [Security],GetAlgNameWStr method, IEnroll2.GetAlgNameWStr, IEnroll2::GetAlgNameWStr, security.ienroll4_getalgnamewstr, xenroll/IEnroll2::GetAlgNameWStr
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
 - IEnroll2::GetAlgNameWStr
 - xenroll/IEnroll2::GetAlgNameWStr
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
 - IEnroll2.GetAlgNameWStr
---

# IEnroll2::GetAlgNameWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetAlgNameWStr</b> method retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

## -parameters

### -param algID [in]

Value representing a cryptographic algorithm, as defined in Wincrypt.h. For example, CALG_MD2 is a defined algorithm identifier. For this method to be successful, the current CSP must support the <i>algID</i> algorithm.

### -param ppwsz [out]

Upon success, pointer to a <b>LPWSTR</b> that represents the name of the algorithm specified by <i>algID</i>.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. If a CSP does not support this method or does not support the <i>algID</i> cryptographic algorithm, an error is returned.

## -remarks

This method may be used to display the names of algorithms whose IDs are retrieved by calling 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs">EnumAlgs</a>.

Constants for the cryptographic algorithms are defined in Wincrypt.h.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>