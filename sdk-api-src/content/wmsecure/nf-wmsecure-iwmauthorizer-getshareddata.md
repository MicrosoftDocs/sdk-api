---
UID: NF:wmsecure.IWMAuthorizer.GetSharedData
title: IWMAuthorizer::GetSharedData (wmsecure.h)
description: Retrieves shared data for the specified certificate.
helpviewer_keywords: ["GetSharedData","GetSharedData method [windows Media Format]","GetSharedData method [windows Media Format]","IWMAuthorizer interface","IWMAuthorizer interface [windows Media Format]","GetSharedData method","IWMAuthorizer.GetSharedData","IWMAuthorizer::GetSharedData","wmformat.iwmauthorizer_getshareddata","wmsecure/IWMAuthorizer::GetSharedData"]
old-location: wmformat\iwmauthorizer_getshareddata.htm
tech.root: wmformat
ms.assetid: 575df33a-b29e-43eb-84c2-6f9875f26196
ms.date: 4/26/2023
ms.keywords: GetSharedData, GetSharedData method [windows Media Format], GetSharedData method [windows Media Format],IWMAuthorizer interface, IWMAuthorizer interface [windows Media Format],GetSharedData method, IWMAuthorizer.GetSharedData, IWMAuthorizer::GetSharedData, wmformat.iwmauthorizer_getshareddata, wmsecure/IWMAuthorizer::GetSharedData
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
 - IWMAuthorizer::GetSharedData
 - wmsecure/IWMAuthorizer::GetSharedData
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
 - IWMAuthorizer.GetSharedData
---

# IWMAuthorizer::GetSharedData


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetSharedData</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

Retrieves shared  data for the specified certificate.

## -parameters

### -param dwCertIndex [in]

### -param pbSharedData [in]

### -param pbCert [in]

### -param ppbSharedData [out]

An address of a pointer to certification data. <i>ppbCertData</i> is allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and must be released by the user.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmauthorizer">IWMAuthorizer</a>