---
UID: NF:qnetwork.IAMChannelInfo.get_ContactEmail
title: IAMChannelInfo::get_ContactEmail (qnetwork.h)
description: The get_ContactEmail method gets the email address of the contact.
helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ContactEmail method","IAMChannelInfo.get_ContactEmail","IAMChannelInfo::get_ContactEmail","IAMChannelInfoget_ContactEmail","dshow.iamchannelinfo_get_contactemail","get_ContactEmail","get_ContactEmail method [DirectShow]","get_ContactEmail method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ContactEmail"]
old-location: dshow\iamchannelinfo_get_contactemail.htm
tech.root: dshow
ms.assetid: a8ab9fc0-1370-44a1-95c8-6592c374d8d6
ms.date: 4/26/2023
ms.keywords: IAMChannelInfo interface [DirectShow],get_ContactEmail method, IAMChannelInfo.get_ContactEmail, IAMChannelInfo::get_ContactEmail, IAMChannelInfoget_ContactEmail, dshow.iamchannelinfo_get_contactemail, get_ContactEmail, get_ContactEmail method [DirectShow], get_ContactEmail method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ContactEmail
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
 - IAMChannelInfo::get_ContactEmail
 - qnetwork/IAMChannelInfo::get_ContactEmail
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
 - IAMChannelInfo.get_ContactEmail
---

# IAMChannelInfo::get_ContactEmail


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_ContactEmail</b> method gets the email address of the contact.

## -parameters

### -param pbstrContactEmail [out]

Receives the contact email.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>