---
UID: NF:wmsecure.IWMSecureChannel.WMSC_AddCertificate
title: IWMSecureChannel::WMSC_AddCertificate (wmsecure.h)
description: The WMSC_AddCertificate method adds certificates that this object can present to other secure channel objects. If no certs are added, then this object can only connect to objects with no signatures.
helpviewer_keywords: ["IWMSecureChannel interface [windows Media Format]","WMSC_AddCertificate method","IWMSecureChannel.WMSC_AddCertificate","IWMSecureChannel::WMSC_AddCertificate","WMSC_AddCertificate","WMSC_AddCertificate method [windows Media Format]","WMSC_AddCertificate method [windows Media Format]","IWMSecureChannel interface","wmformat.iwmsecurechannel_wmsc_addcertificate","wmsecure/IWMSecureChannel::WMSC_AddCertificate"]
old-location: wmformat\iwmsecurechannel_wmsc_addcertificate.htm
tech.root: wmformat
ms.assetid: 0e5fbd9e-1669-4e0e-90b6-1542cc6d2ae4
ms.date: 12/05/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_AddCertificate method, IWMSecureChannel.WMSC_AddCertificate, IWMSecureChannel::WMSC_AddCertificate, WMSC_AddCertificate, WMSC_AddCertificate method [windows Media Format], WMSC_AddCertificate method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_addcertificate, wmsecure/IWMSecureChannel::WMSC_AddCertificate
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSecureChannel::WMSC_AddCertificate
 - wmsecure/IWMSecureChannel::WMSC_AddCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel.WMSC_AddCertificate
---

# IWMSecureChannel::WMSC_AddCertificate


## -description

<p class="CCE_Message">[<b>WMSC_AddCertificate</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>WMSC_AddCertificate</b> method adds certificates that this object can present to other secure channel objects.
     If no certs are added, then this object can only connect to objects with
     no signatures.

## -parameters

### -param pCert [in]

A pointer to an authorizer object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>