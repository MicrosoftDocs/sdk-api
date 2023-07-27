---
UID: NF:vmr9.IVMRFilterConfig9.GetRenderingMode
title: IVMRFilterConfig9::GetRenderingMode (vmr9.h)
description: The GetRenderingMode method retrieves the rendering mode currently being used by the VMR.
helpviewer_keywords: ["GetRenderingMode","GetRenderingMode method [DirectShow]","GetRenderingMode method [DirectShow]","IVMRFilterConfig9 interface","IVMRFilterConfig9 interface [DirectShow]","GetRenderingMode method","IVMRFilterConfig9.GetRenderingMode","IVMRFilterConfig9::GetRenderingMode","IVMRFilterConfig9GetRenderingMode","dshow.ivmrfilterconfig9_getrenderingmode","vmr9/IVMRFilterConfig9::GetRenderingMode"]
old-location: dshow\ivmrfilterconfig9_getrenderingmode.htm
tech.root: dshow
ms.assetid: e39077ce-737f-4dd9-ab7d-4dc087828fdf
ms.date: 4/26/2023
ms.keywords: GetRenderingMode, GetRenderingMode method [DirectShow], GetRenderingMode method [DirectShow],IVMRFilterConfig9 interface, IVMRFilterConfig9 interface [DirectShow],GetRenderingMode method, IVMRFilterConfig9.GetRenderingMode, IVMRFilterConfig9::GetRenderingMode, IVMRFilterConfig9GetRenderingMode, dshow.ivmrfilterconfig9_getrenderingmode, vmr9/IVMRFilterConfig9::GetRenderingMode
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRFilterConfig9::GetRenderingMode
 - vmr9/IVMRFilterConfig9::GetRenderingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRFilterConfig9.GetRenderingMode
---

# IVMRFilterConfig9::GetRenderingMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRenderingMode</code> method retrieves the rendering mode currently being used by the VMR.

## -parameters

### -param pMode [out]

Receives a member of the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9mode">VMR9Mode</a> enumeration.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<i>pMode</i> is invalid

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>