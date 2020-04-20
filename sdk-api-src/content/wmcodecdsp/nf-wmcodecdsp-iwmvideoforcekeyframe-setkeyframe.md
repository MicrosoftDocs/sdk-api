---
UID: NF:wmcodecdsp.IWMVideoForceKeyFrame.SetKeyFrame
title: IWMVideoForceKeyFrame::SetKeyFrame (wmcodecdsp.h)
description: Specifies that the current frame will be encoded as a key frame.helpviewer_keywords: ["IWMVideoForceKeyFrame interface [Media Foundation]","SetKeyFrame method","IWMVideoForceKeyFrame.SetKeyFrame","IWMVideoForceKeyFrame::SetKeyFrame","SetKeyFrame","SetKeyFrame method [Media Foundation]","SetKeyFrame method [Media Foundation]","IWMVideoForceKeyFrame interface","codecapi.iwmvideoforcekeyframe_setkeyframe","codecapi.iwmvideoforcekeyframesetkeyframe","mf.iwmvideoforcekeyframesetkeyframe","wmcodecdsp/IWMVideoForceKeyFrame::SetKeyFrame"]
old-location: mf\iwmvideoforcekeyframesetkeyframe.htm
tech.root: medfound
ms.assetid: 5cfebe9f-45b1-4cba-8813-6c9405657323
ms.date: 12/05/2018
ms.keywords: IWMVideoForceKeyFrame interface [Media Foundation],SetKeyFrame method, IWMVideoForceKeyFrame.SetKeyFrame, IWMVideoForceKeyFrame::SetKeyFrame, SetKeyFrame, SetKeyFrame method [Media Foundation], SetKeyFrame method [Media Foundation],IWMVideoForceKeyFrame interface, codecapi.iwmvideoforcekeyframe_setkeyframe, codecapi.iwmvideoforcekeyframesetkeyframe, mf.iwmvideoforcekeyframesetkeyframe, wmcodecdsp/IWMVideoForceKeyFrame::SetKeyFrame
f1_keywords:
- wmcodecdsp/IWMVideoForceKeyFrame.SetKeyFrame
dev_langs:
- c++
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmcodecdsp.h
api_name:
- IWMVideoForceKeyFrame.SetKeyFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMVideoForceKeyFrame::SetKeyFrame


## -description


Specifies that the current frame will be encoded as a key frame.




## -parameters






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
</table>
 




## -remarks



To force the encoder to make the current frame a key frame, call this method before calling <b>IMediaObject::ProcessOutput</b> or <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.



Each call to this method applies to a single frame. After processing this frame, the encoder resumes automatically assigning key frames (bounded by the maximum key frame distance).






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideoforcekeyframe">IWMVideoForceKeyFrame Interface</a>
 

 

