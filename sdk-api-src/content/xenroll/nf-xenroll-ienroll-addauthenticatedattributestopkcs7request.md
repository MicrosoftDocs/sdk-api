---
UID: NF:xenroll.IEnroll.AddAuthenticatedAttributesToPKCS7Request
title: IEnroll::AddAuthenticatedAttributesToPKCS7Request (xenroll.h)
description: The AddAuthenticatedAttributesToPKCS7Request method adds authenticated attributes to a PKCS
old-location: security\ienroll4_addauthenticatedattributestopkcs7request.htm
tech.root: SecCrypto
ms.assetid: a65eca3d-8308-4bdc-b851-016a4e63a1f1
ms.date: 12/05/2018
ms.keywords: AddAuthenticatedAttributesToPKCS7Request, AddAuthenticatedAttributesToPKCS7Request method [Security], AddAuthenticatedAttributesToPKCS7Request method [Security],IEnroll interface, IEnroll interface [Security],AddAuthenticatedAttributesToPKCS7Request method, IEnroll.AddAuthenticatedAttributesToPKCS7Request, IEnroll::AddAuthenticatedAttributesToPKCS7Request, security.ienroll4_addauthenticatedattributestopkcs7request, xenroll/IEnroll::AddAuthenticatedAttributesToPKCS7Request
f1_keywords:
- xenroll/IEnroll.AddAuthenticatedAttributesToPKCS7Request
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Xenroll.dll
api_name:
- IEnroll.AddAuthenticatedAttributesToPKCS7Request
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::AddAuthenticatedAttributesToPKCS7Request


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddAuthenticatedAttributesToPKCS7Request</b> method adds authenticated attributes to a PKCS #7 certificate request. This method was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.


## -parameters




### -param pAttributes [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure that represents the authenticated attributes to add to the PKCS #7 certificate request.


## -returns



The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
 

 

