---
UID: NF:qnetwork.IAMExtendedErrorInfo.get_ErrorCode
title: IAMExtendedErrorInfo::get_ErrorCode (qnetwork.h)
description: The get_ErrorCode method retrieves the current error code.
helpviewer_keywords: ["IAMExtendedErrorInfo interface [DirectShow]","get_ErrorCode method","IAMExtendedErrorInfo.get_ErrorCode","IAMExtendedErrorInfo::get_ErrorCode","IAMExtendedErrorInfoget_ErrorCode","dshow.iamextendederrorinfo_get_errorcode","get_ErrorCode","get_ErrorCode method [DirectShow]","get_ErrorCode method [DirectShow]","IAMExtendedErrorInfo interface","qnetwork/IAMExtendedErrorInfo::get_ErrorCode"]
old-location: dshow\iamextendederrorinfo_get_errorcode.htm
tech.root: dshow
ms.assetid: e7ab81a5-bc62-48f5-a2c8-ee53e86aea89
ms.date: 4/26/2023
ms.keywords: IAMExtendedErrorInfo interface [DirectShow],get_ErrorCode method, IAMExtendedErrorInfo.get_ErrorCode, IAMExtendedErrorInfo::get_ErrorCode, IAMExtendedErrorInfoget_ErrorCode, dshow.iamextendederrorinfo_get_errorcode, get_ErrorCode, get_ErrorCode method [DirectShow], get_ErrorCode method [DirectShow],IAMExtendedErrorInfo interface, qnetwork/IAMExtendedErrorInfo::get_ErrorCode
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
 - IAMExtendedErrorInfo::get_ErrorCode
 - qnetwork/IAMExtendedErrorInfo::get_ErrorCode
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
 - IAMExtendedErrorInfo.get_ErrorCode
---

# IAMExtendedErrorInfo::get_ErrorCode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ErrorCode</code> method retrieves the current error code.

## -parameters

### -param pErrorCode [out]

Pointer to a variable that receives the error code.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendederrorinfo">IAMExtendedErrorInfo Interface</a>