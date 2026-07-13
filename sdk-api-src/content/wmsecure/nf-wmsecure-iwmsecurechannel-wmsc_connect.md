---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Connect
title: IWMSecureChannel::WMSC_Connect (wmsecure.h)
description: The WMSC_Connect method initializes the secure connection.
helpviewer_keywords: ["IWMSecureChannel interface [windows Media Format]","WMSC_Connect method","IWMSecureChannel.WMSC_Connect","IWMSecureChannel::WMSC_Connect","WMSC_Connect","WMSC_Connect method [windows Media Format]","WMSC_Connect method [windows Media Format]","IWMSecureChannel interface","wmformat.iwmsecurechannel_wmsc_connect","wmsecure/IWMSecureChannel::WMSC_Connect"]
old-location: wmformat\iwmsecurechannel_wmsc_connect.htm
tech.root: wmformat
ms.assetid: d8386b23-6319-4687-9de2-a81e661a60e6
ms.date: 4/26/2023
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_Connect method, IWMSecureChannel.WMSC_Connect, IWMSecureChannel::WMSC_Connect, WMSC_Connect, WMSC_Connect method [windows Media Format], WMSC_Connect method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_connect, wmsecure/IWMSecureChannel::WMSC_Connect
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
 - IWMSecureChannel::WMSC_Connect
 - wmsecure/IWMSecureChannel::WMSC_Connect
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
 - IWMSecureChannel.WMSC_Connect
---

# IWMSecureChannel::WMSC_Connect


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>WMSC_Connect</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>WMSC_Connect</b> method initializes the secure connection.

## -parameters

### -param pOtherSide [in]

Pointer to a secure channel object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 This function allow each side of the channel to validate the other side before  sharing the secret that will be used for encryption.
    In addition, the DLL serializers used to 
     serialize the encryption become shared.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>