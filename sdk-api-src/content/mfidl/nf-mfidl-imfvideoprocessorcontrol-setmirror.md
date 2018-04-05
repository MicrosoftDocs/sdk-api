---
UID: NF:mfidl.IMFVideoProcessorControl.SetMirror
title: IMFVideoProcessorControl::SetMirror method
author: windows-driver-content
description: Specifies whether to flip the video image.
old-location: mf\imfvideoprocessorcontrol_setmirror.htm
old-project: medfound
ms.assetid: 4529FEE5-7FDF-4EFF-93C1-E20A63186496
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMFVideoProcessorControl, IMFVideoProcessorControl interface [Media Foundation], SetMirror method, IMFVideoProcessorControl::SetMirror, SetMirror method [Media Foundation], SetMirror method [Media Foundation], IMFVideoProcessorControl interface, SetMirror,IMFVideoProcessorControl.SetMirror, mf.imfvideoprocessorcontrol_setmirror, mfidl/IMFVideoProcessorControl::SetMirror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFVideoProcessorControl.SetMirror
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoProcessorControl::SetMirror method


## -description


Specifies whether to flip the video image.


## -parameters




### -param eMirror

An <a href="https://msdn.microsoft.com/AFD29AD7-8DC9-4834-8F8E-D062A3A19BD0">MF_VIDEO_PROCESSOR_MIRROR</a> value that specifies whether to flip the video image, either horizontally or vertically.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>
 

 

