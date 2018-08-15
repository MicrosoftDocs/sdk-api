---
UID: NF:wmsdkidl.IWMVideoMediaProps.SetMaxKeyFrameSpacing
title: IWMVideoMediaProps::SetMaxKeyFrameSpacing
author: windows-sdk-content
description: The SetMaxKeyFrameSpacing method specifies the maximum interval between key frames.
old-location: wmformat\iwmvideomediaprops_setmaxkeyframespacing.htm
old-project: wmformat
ms.assetid: 1d1a9090-2658-45bd-8893-30e063d10aa8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMVideoMediaProps interface [windows Media Format],SetMaxKeyFrameSpacing method, IWMVideoMediaProps.SetMaxKeyFrameSpacing, IWMVideoMediaProps::SetMaxKeyFrameSpacing, IWMVideoMediaPropsSetMaxKeyFrameSpacing, SetMaxKeyFrameSpacing, SetMaxKeyFrameSpacing method [windows Media Format], SetMaxKeyFrameSpacing method [windows Media Format],IWMVideoMediaProps interface, wmformat.iwmvideomediaprops_setmaxkeyframespacing, wmsdkidl/IWMVideoMediaProps::SetMaxKeyFrameSpacing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
api_name:
 - IWMVideoMediaProps.SetMaxKeyFrameSpacing
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMVideoMediaProps::SetMaxKeyFrameSpacing


## -description



The <b>SetMaxKeyFrameSpacing</b> method specifies the maximum interval between key frames.




## -parameters




### -param llTime [in]

Maximum key-frame spacing in 100-nanosecond units.


## -returns



This method always returns S_OK.




## -remarks



A key frame is a video frame that can be rendered without any information being required from any previous frame. A delta frame is a frame that is dependent on a previous frame. The application can seek to a key frame, but not to a delta frame. The SDK does not enforce any limit on the time between key frames. In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally. For recommended values, see <a href="https://msdn.microsoft.com/2df507f9-60a5-4489-b3db-7fe15604e625">Configuring Video Streams for Seeking Performance</a>.




## -see-also




<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/125d352e-b181-4baa-8763-21315534beea">IWMVideoMediaProps::GetMaxKeyFrameSpacing</a>
 

 

