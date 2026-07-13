---
UID: NF:xenroll.IEnroll.put_DeleteRequestCert
title: IEnroll::put_DeleteRequestCert (xenroll.h)
description: The DeleteRequestCert property of IEnroll4 sets or retrieves a Boolean value that determines whether dummy certificates in the request store are deleted. (Put)
helpviewer_keywords: ["DeleteRequestCert property [Security]","DeleteRequestCert property [Security]","IEnroll interface","IEnroll interface [Security]","DeleteRequestCert property","IEnroll.DeleteRequestCert","IEnroll.put_DeleteRequestCert","IEnroll::DeleteRequestCert","IEnroll::get_DeleteRequestCert","IEnroll::put_DeleteRequestCert","put_DeleteRequestCert","security.ienroll4_deleterequestcert","xenroll/IEnroll::DeleteRequestCert","xenroll/IEnroll::get_DeleteRequestCert","xenroll/IEnroll::put_DeleteRequestCert"]
old-location: security\ienroll4_deleterequestcert.htm
tech.root: security
ms.assetid: 54b85347-cdc1-42e3-bc26-0b50bd58131a
ms.date: 12/05/2018
ms.keywords: DeleteRequestCert property [Security], DeleteRequestCert property [Security],IEnroll interface, IEnroll interface [Security],DeleteRequestCert property, IEnroll.DeleteRequestCert, IEnroll.put_DeleteRequestCert, IEnroll::DeleteRequestCert, IEnroll::get_DeleteRequestCert, IEnroll::put_DeleteRequestCert, put_DeleteRequestCert, security.ienroll4_deleterequestcert, xenroll/IEnroll::DeleteRequestCert, xenroll/IEnroll::get_DeleteRequestCert, xenroll/IEnroll::put_DeleteRequestCert
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
 - IEnroll::put_DeleteRequestCert
 - xenroll/IEnroll::put_DeleteRequestCert
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
 - IEnroll.DeleteRequestCert
 - IEnroll.get_DeleteRequestCert
 - IEnroll.put_DeleteRequestCert
---

# IEnroll::put_DeleteRequestCert


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>DeleteRequestCert</b> property sets or retrieves a Boolean value that  determines whether dummy certificates in the request store are deleted.

Dummy certificates are created for the purpose of persisting the keys generated for the PKCS #10 request during the enrollment process. The store specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a> property is where the dummy certificate is created. The newly generated keys are added as properties to the dummy certificate to persist them until a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> processes the request and responds with a PKCS #7. On acceptance of the PKCS #7, the dummy certificate is removed and the keys are added as properties of the issued certificate returned by the certification authority. For debugging and testing, it is often desirable to not delete the dummy certificate. Setting <b>DeleteRequestCert</b> to false prevents its deletion.

The default value for this property is  true. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>DeleteRequestCert</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
