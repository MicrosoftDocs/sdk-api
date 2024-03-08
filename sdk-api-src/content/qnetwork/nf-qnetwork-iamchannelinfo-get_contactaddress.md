---
UID: NF:qnetwork.IAMChannelInfo.get_ContactAddress
title: IAMChannelInfo::get_ContactAddress (qnetwork.h)
description: The get_ContactAddress method retrieves the contact address.
helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ContactAddress method","IAMChannelInfo.get_ContactAddress","IAMChannelInfo::get_ContactAddress","IAMChannelInfoget_ContactAddress","dshow.iamchannelinfo_get_contactaddress","get_ContactAddress","get_ContactAddress method [DirectShow]","get_ContactAddress method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ContactAddress"]
old-location: dshow\iamchannelinfo_get_contactaddress.htm
tech.root: dshow
ms.assetid: b94ccc71-92d1-4c1a-b34a-c34e6ea7bd91
ms.date: 4/26/2023
ms.keywords: IAMChannelInfo interface [DirectShow],get_ContactAddress method, IAMChannelInfo.get_ContactAddress, IAMChannelInfo::get_ContactAddress, IAMChannelInfoget_ContactAddress, dshow.iamchannelinfo_get_contactaddress, get_ContactAddress, get_ContactAddress method [DirectShow], get_ContactAddress method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ContactAddress
req.header: qnetwork.h
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
 - IAMChannelInfo::get_ContactAddress
 - qnetwork/IAMChannelInfo::get_ContactAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMChannelInfo.get_ContactAddress
---

# IAMChannelInfo::get_ContactAddress


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ContactAddress</code> method retrieves the contact address.

## -parameters

### -param pbstrContactAddress [out]

Pointer to a variable that receives the contact address.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>