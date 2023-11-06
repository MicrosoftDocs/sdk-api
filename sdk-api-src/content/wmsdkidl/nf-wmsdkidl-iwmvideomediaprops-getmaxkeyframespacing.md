---
UID: NF:wmsdkidl.IWMVideoMediaProps.GetMaxKeyFrameSpacing
title: IWMVideoMediaProps::GetMaxKeyFrameSpacing (wmsdkidl.h)
description: The GetMaxKeyFrameSpacing method retrieves the maximum interval between key frames.
helpviewer_keywords: ["GetMaxKeyFrameSpacing","GetMaxKeyFrameSpacing method [windows Media Format]","GetMaxKeyFrameSpacing method [windows Media Format]","IWMVideoMediaProps interface","IWMVideoMediaProps interface [windows Media Format]","GetMaxKeyFrameSpacing method","IWMVideoMediaProps.GetMaxKeyFrameSpacing","IWMVideoMediaProps::GetMaxKeyFrameSpacing","IWMVideoMediaPropsGetMaxKeyFrameSpacing","wmformat.iwmvideomediaprops_getmaxkeyframespacing","wmsdkidl/IWMVideoMediaProps::GetMaxKeyFrameSpacing"]
old-location: wmformat\iwmvideomediaprops_getmaxkeyframespacing.htm
tech.root: wmformat
ms.assetid: 125d352e-b181-4baa-8763-21315534beea
ms.date: 4/26/2023
ms.keywords: GetMaxKeyFrameSpacing, GetMaxKeyFrameSpacing method [windows Media Format], GetMaxKeyFrameSpacing method [windows Media Format],IWMVideoMediaProps interface, IWMVideoMediaProps interface [windows Media Format],GetMaxKeyFrameSpacing method, IWMVideoMediaProps.GetMaxKeyFrameSpacing, IWMVideoMediaProps::GetMaxKeyFrameSpacing, IWMVideoMediaPropsGetMaxKeyFrameSpacing, wmformat.iwmvideomediaprops_getmaxkeyframespacing, wmsdkidl/IWMVideoMediaProps::GetMaxKeyFrameSpacing
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
 - IWMVideoMediaProps::GetMaxKeyFrameSpacing
 - wmsdkidl/IWMVideoMediaProps::GetMaxKeyFrameSpacing
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
 - IWMVideoMediaProps.GetMaxKeyFrameSpacing
---

# IWMVideoMediaProps::GetMaxKeyFrameSpacing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMaxKeyFrameSpacing</b> method retrieves the maximum interval between key frames.

## -parameters

### -param pllTime [out]

Pointer to a variable that receives the interval in 100-nanosecond units.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pllTime</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method retrieves the value set by <b>SetMaxKeyFrameSpacing</b>, or the default value for the key frame spacing, during the encoding process only. If called for a file that is open in the reader, the method always returns zero.

For more information, see the Remarks for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing">SetMaxKeyFrameSpacing</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps Interface</a>