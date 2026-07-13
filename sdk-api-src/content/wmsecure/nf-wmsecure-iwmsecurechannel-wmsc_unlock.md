---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Unlock
title: IWMSecureChannel::WMSC_Unlock (wmsecure.h)
description: The WMSC_Unlock method unlocks access to the secure connection.
helpviewer_keywords: ["IWMSecureChannel interface [windows Media Format]","WMSC_Unlock method","IWMSecureChannel.WMSC_Unlock","IWMSecureChannel::WMSC_Unlock","WMSC_Unlock","WMSC_Unlock method [windows Media Format]","WMSC_Unlock method [windows Media Format]","IWMSecureChannel interface","wmformat.iwmsecurechannel_wmsc_unlock","wmsecure/IWMSecureChannel::WMSC_Unlock"]
old-location: wmformat\iwmsecurechannel_wmsc_unlock.htm
tech.root: wmformat
ms.assetid: 3127a3bb-380d-46f9-82a3-d584705b1c60
ms.date: 4/26/2023
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_Unlock method, IWMSecureChannel.WMSC_Unlock, IWMSecureChannel::WMSC_Unlock, WMSC_Unlock, WMSC_Unlock method [windows Media Format], WMSC_Unlock method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_unlock, wmsecure/IWMSecureChannel::WMSC_Unlock
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
 - IWMSecureChannel::WMSC_Unlock
 - wmsecure/IWMSecureChannel::WMSC_Unlock
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
 - IWMSecureChannel.WMSC_Unlock
---

# IWMSecureChannel::WMSC_Unlock


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>WMSC_Unlock</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>WMSC_Unlock</b> method unlocks access to the secure connection.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>
