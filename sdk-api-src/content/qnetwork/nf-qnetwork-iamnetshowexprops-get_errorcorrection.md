---
UID: NF:qnetwork.IAMNetShowExProps.get_ErrorCorrection
title: IAMNetShowExProps::get_ErrorCorrection (qnetwork.h)
description: The get_ErrorCorrection method retrieves the current error correction method.
helpviewer_keywords: ["IAMNetShowExProps interface [DirectShow]","get_ErrorCorrection method","IAMNetShowExProps.get_ErrorCorrection","IAMNetShowExProps::get_ErrorCorrection","IAMNetShowExPropsget_ErrorCorrection","dshow.iamnetshowexprops_get_errorcorrection","get_ErrorCorrection","get_ErrorCorrection method [DirectShow]","get_ErrorCorrection method [DirectShow]","IAMNetShowExProps interface","qnetwork/IAMNetShowExProps::get_ErrorCorrection"]
old-location: dshow\iamnetshowexprops_get_errorcorrection.htm
tech.root: dshow
ms.assetid: ab731d68-969b-425d-978a-879b15c06a88
ms.date: 4/26/2023
ms.keywords: IAMNetShowExProps interface [DirectShow],get_ErrorCorrection method, IAMNetShowExProps.get_ErrorCorrection, IAMNetShowExProps::get_ErrorCorrection, IAMNetShowExPropsget_ErrorCorrection, dshow.iamnetshowexprops_get_errorcorrection, get_ErrorCorrection, get_ErrorCorrection method [DirectShow], get_ErrorCorrection method [DirectShow],IAMNetShowExProps interface, qnetwork/IAMNetShowExProps::get_ErrorCorrection
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
 - IAMNetShowExProps::get_ErrorCorrection
 - qnetwork/IAMNetShowExProps::get_ErrorCorrection
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
 - IAMNetShowExProps.get_ErrorCorrection
---

# IAMNetShowExProps::get_ErrorCorrection


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ErrorCorrection</code> method retrieves the current error correction method.

## -parameters

### -param pbstrErrorCorrection

Pointer to a variable that receives a string describing the error correction method.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>