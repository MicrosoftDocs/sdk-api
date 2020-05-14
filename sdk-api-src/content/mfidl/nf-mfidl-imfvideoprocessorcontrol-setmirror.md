---
UID: NF:mfidl.IMFVideoProcessorControl.SetMirror
title: IMFVideoProcessorControl::SetMirror (mfidl.h)
description: Specifies whether to flip the video image.helpviewer_keywords: ["IMFVideoProcessorControl interface [Media Foundation]","SetMirror method","IMFVideoProcessorControl.SetMirror","IMFVideoProcessorControl::SetMirror","SetMirror","SetMirror method [Media Foundation]","SetMirror method [Media Foundation]","IMFVideoProcessorControl interface","mf.imfvideoprocessorcontrol_setmirror","mfidl/IMFVideoProcessorControl::SetMirror"]
old-location: mf\imfvideoprocessorcontrol_setmirror.htm
tech.root: medfound
ms.assetid: 4529FEE5-7FDF-4EFF-93C1-E20A63186496
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetMirror method, IMFVideoProcessorControl.SetMirror, IMFVideoProcessorControl::SetMirror, SetMirror, SetMirror method [Media Foundation], SetMirror method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setmirror, mfidl/IMFVideoProcessorControl::SetMirror
f1_keywords:
- mfidl/IMFVideoProcessorControl.SetMirror
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- mfidl.h
api_name:
- IMFVideoProcessorControl.SetMirror
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessorControl::SetMirror


## -description


Specifies whether to flip the video image.


## -parameters




### -param eMirror

An <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ne-mfidl-mf_video_processor_mirror">MF_VIDEO_PROCESSOR_MIRROR</a> value that specifies whether to flip the video image, either horizontally or vertically.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>
 

 

