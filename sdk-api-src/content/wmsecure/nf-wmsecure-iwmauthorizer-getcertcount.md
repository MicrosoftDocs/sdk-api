---
UID: NF:wmsecure.IWMAuthorizer.GetCertCount
title: IWMAuthorizer::GetCertCount (wmsecure.h)
description: Get the number of certificates.helpviewer_keywords: ["GetCertCount","GetCertCount method [windows Media Format]","GetCertCount method [windows Media Format]","IWMAuthorizer interface","IWMAuthorizer interface [windows Media Format]","GetCertCount method","IWMAuthorizer.GetCertCount","IWMAuthorizer::GetCertCount","wmformat.iwmauthorizer_getcertcount","wmsecure/IWMAuthorizer::GetCertCount"]
old-location: wmformat\iwmauthorizer_getcertcount.htm
tech.root: wmformat
ms.assetid: afe8a924-3d2b-42e6-9700-a6075f51ff10
ms.date: 12/05/2018
ms.keywords: GetCertCount, GetCertCount method [windows Media Format], GetCertCount method [windows Media Format],IWMAuthorizer interface, IWMAuthorizer interface [windows Media Format],GetCertCount method, IWMAuthorizer.GetCertCount, IWMAuthorizer::GetCertCount, wmformat.iwmauthorizer_getcertcount, wmsecure/IWMAuthorizer::GetCertCount
f1_keywords:
- wmsecure/IWMAuthorizer.GetCertCount
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmsecure.h
api_name:
- IWMAuthorizer.GetCertCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMAuthorizer::GetCertCount


## -description


<p class="CCE_Message">[<b>GetCertCount</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

Get the number of certificates.


## -parameters




### -param pcCerts [out]

Receives a pointer to a count of certs.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmauthorizer">IWMAuthorizer</a>
 

 

