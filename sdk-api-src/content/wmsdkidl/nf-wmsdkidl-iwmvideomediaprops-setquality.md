---
UID: NF:wmsdkidl.IWMVideoMediaProps.SetQuality
title: IWMVideoMediaProps::SetQuality (wmsdkidl.h)
description: The SetQuality method specifies the quality setting for the video stream.
helpviewer_keywords: ["IWMVideoMediaProps interface [windows Media Format]","SetQuality method","IWMVideoMediaProps.SetQuality","IWMVideoMediaProps::SetQuality","IWMVideoMediaPropsSetQuality","SetQuality","SetQuality method [windows Media Format]","SetQuality method [windows Media Format]","IWMVideoMediaProps interface","wmformat.iwmvideomediaprops_setquality","wmsdkidl/IWMVideoMediaProps::SetQuality"]
old-location: wmformat\iwmvideomediaprops_setquality.htm
tech.root: wmformat
ms.assetid: 0f91380d-b8c8-47db-99ca-12c897bdff20
ms.date: 4/26/2023
ms.keywords: IWMVideoMediaProps interface [windows Media Format],SetQuality method, IWMVideoMediaProps.SetQuality, IWMVideoMediaProps::SetQuality, IWMVideoMediaPropsSetQuality, SetQuality, SetQuality method [windows Media Format], SetQuality method [windows Media Format],IWMVideoMediaProps interface, wmformat.iwmvideomediaprops_setquality, wmsdkidl/IWMVideoMediaProps::SetQuality
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMVideoMediaProps::SetQuality
 - wmsdkidl/IWMVideoMediaProps::SetQuality
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
api_name:
 - IWMVideoMediaProps.SetQuality
---

# IWMVideoMediaProps::SetQuality


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetQuality</b> method specifies the quality setting for the video stream.

## -parameters

### -param dwQuality [in]

<b>DWORD</b> specifying the quality setting, in the range from zero (maximum <a href="/windows/desktop/wmformat/wmformat-glossary">frame rate</a>) to 100 (maximum image quality).

## -returns

This method always returns S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-getquality">IWMVideoMediaProps::GetQuality</a>