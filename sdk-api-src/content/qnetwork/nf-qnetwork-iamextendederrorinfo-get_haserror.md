---
UID: NF:qnetwork.IAMExtendedErrorInfo.get_HasError
title: IAMExtendedErrorInfo::get_HasError (qnetwork.h)
description: The get_HasError method queries whether an error occurred.
helpviewer_keywords: ["IAMExtendedErrorInfo interface [DirectShow]","get_HasError method","IAMExtendedErrorInfo.get_HasError","IAMExtendedErrorInfo::get_HasError","IAMExtendedErrorInfoget_HasError","dshow.iamextendederrorinfo_get_haserror","get_HasError","get_HasError method [DirectShow]","get_HasError method [DirectShow]","IAMExtendedErrorInfo interface","qnetwork/IAMExtendedErrorInfo::get_HasError"]
old-location: dshow\iamextendederrorinfo_get_haserror.htm
tech.root: dshow
ms.assetid: 8aad2849-5a99-484a-8830-e014672e62fb
ms.date: 4/26/2023
ms.keywords: IAMExtendedErrorInfo interface [DirectShow],get_HasError method, IAMExtendedErrorInfo.get_HasError, IAMExtendedErrorInfo::get_HasError, IAMExtendedErrorInfoget_HasError, dshow.iamextendederrorinfo_get_haserror, get_HasError, get_HasError method [DirectShow], get_HasError method [DirectShow],IAMExtendedErrorInfo interface, qnetwork/IAMExtendedErrorInfo::get_HasError
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
 - IAMExtendedErrorInfo::get_HasError
 - qnetwork/IAMExtendedErrorInfo::get_HasError
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
 - IAMExtendedErrorInfo.get_HasError
---

# IAMExtendedErrorInfo::get_HasError


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_HasError</code> method queries whether an error occurred.

## -parameters

### -param pHasError

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>No error.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>An error occurred.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>pHasError</i> is true, you can call the <b>get_ErrorCode</b> and <b>get_ErrorDescription</b> methods to determine the nature of the error.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendederrorinfo">IAMExtendedErrorInfo Interface</a>