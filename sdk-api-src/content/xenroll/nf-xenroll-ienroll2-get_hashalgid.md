---
UID: NF:xenroll.IEnroll2.get_HashAlgID
title: IEnroll2::get_HashAlgID (xenroll.h)
description: The HashAlgID property of IEnroll4 sets or retrieves the hash algorithm used when signing a PKCS (Get)
helpviewer_keywords: ["HashAlgID property [Security]","HashAlgID property [Security]","IEnroll2 interface","HashAlgID property [Security]","IEnroll4 interface","IEnroll2 interface [Security]","HashAlgID property","IEnroll2.HashAlgID","IEnroll2.get_HashAlgID","IEnroll2::HashAlgID","IEnroll2::get_HashAlgID","IEnroll2::put_HashAlgID","IEnroll4 interface [Security]","HashAlgID property","IEnroll4.HashAlgID","IEnroll4::get_HashAlgID","IEnroll4::put_HashAlgID","get_HashAlgID","put_HashAlgID","security.ienroll4_hashalgid","xenroll/IEnroll2::HashAlgID","xenroll/IEnroll2::get_HashAlgID","xenroll/IEnroll2::put_HashAlgID","xenroll/IEnroll4::HashAlgID","xenroll/IEnroll4::get_HashAlgID","xenroll/IEnroll4::put_HashAlgID"]
old-location: security\ienroll4_hashalgid.htm
tech.root: security
ms.assetid: ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e
ms.date: 12/05/2018
ms.keywords: HashAlgID property [Security], HashAlgID property [Security],IEnroll2 interface, HashAlgID property [Security],IEnroll4 interface, IEnroll2 interface [Security],HashAlgID property, IEnroll2.HashAlgID, IEnroll2.get_HashAlgID, IEnroll2::HashAlgID, IEnroll2::get_HashAlgID, IEnroll2::put_HashAlgID, IEnroll4 interface [Security],HashAlgID property, IEnroll4.HashAlgID, IEnroll4::get_HashAlgID, IEnroll4::put_HashAlgID, get_HashAlgID, put_HashAlgID, security.ienroll4_hashalgid, xenroll/IEnroll2::HashAlgID, xenroll/IEnroll2::get_HashAlgID, xenroll/IEnroll2::put_HashAlgID, xenroll/IEnroll4::HashAlgID, xenroll/IEnroll4::get_HashAlgID, xenroll/IEnroll4::put_HashAlgID
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
 - IEnroll2::get_HashAlgID
 - xenroll/IEnroll2::get_HashAlgID
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
 - IEnroll2.HashAlgID
 - IEnroll2.get_HashAlgID
 - IEnroll2.put_HashAlgID
 - IEnroll4.HashAlgID
 - IEnroll4.get_HashAlgID
 - IEnroll4.put_HashAlgID
---

# IEnroll2::get_HashAlgID


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgID</b> property sets or retrieves the <a href="/windows/desktop/SecGloss/h-gly">hash algorithm</a> used when signing a PKCS #10 <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

This property was first introduced in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

The values for this property are <a href="/windows/desktop/SecGloss/h-gly">hash algorithm</a> IDs, such as those returned by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs">EnumAlgs</a> method. If both the <b>HashAlgID</b> and 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr">HashAlgorithmWStr</a> properties are set, whichever has been updated most recently determines the hash algorithm used to sign the PKCS #10 request.

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
