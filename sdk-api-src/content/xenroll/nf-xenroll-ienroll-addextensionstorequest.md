---
UID: NF:xenroll.IEnroll.AddExtensionsToRequest
title: IEnroll::AddExtensionsToRequest (xenroll.h)
description: The AddExtensionsToRequest method adds extensions to the certificate request. This method was first defined in the IEnroll interface.
helpviewer_keywords: ["AddExtensionsToRequest","AddExtensionsToRequest method [Security]","AddExtensionsToRequest method [Security]","IEnroll interface","IEnroll interface [Security]","AddExtensionsToRequest method","IEnroll.AddExtensionsToRequest","IEnroll::AddExtensionsToRequest","security.ienroll4_addextensionstorequest","xenroll/IEnroll::AddExtensionsToRequest"]
old-location: security\ienroll4_addextensionstorequest.htm
tech.root: security
ms.assetid: 6976fd52-98f0-4eff-aa83-7cf5cb5d5e67
ms.date: 12/05/2018
ms.keywords: AddExtensionsToRequest, AddExtensionsToRequest method [Security], AddExtensionsToRequest method [Security],IEnroll interface, IEnroll interface [Security],AddExtensionsToRequest method, IEnroll.AddExtensionsToRequest, IEnroll::AddExtensionsToRequest, security.ienroll4_addextensionstorequest, xenroll/IEnroll::AddExtensionsToRequest
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
 - IEnroll::AddExtensionsToRequest
 - xenroll/IEnroll::AddExtensionsToRequest
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
 - IEnroll.AddExtensionsToRequest
---

# IEnroll::AddExtensionsToRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddExtensionsToRequest</b> method adds extensions to the certificate request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param pCertExtensions [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extensions">CERT_EXTENSIONS</a> structure that represents the extensions to add to the request.

## -returns

The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>