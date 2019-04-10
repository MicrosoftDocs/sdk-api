---
UID: NF:wmsdkidl.IWMBandwidthSharing.SetBandwidth
title: IWMBandwidthSharing::SetBandwidth (wmsdkidl.h)
author: windows-sdk-content
description: The SetBandwidth method sets the bandwidth and maximum buffer size for a combined stream.
old-location: wmformat\iwmbandwidthsharing_setbandwidth.htm
tech.root: wmformat
ms.assetid: 1f2ac613-3674-46d9-ae7c-26389dbede02
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMBandwidthSharing interface [windows Media Format],SetBandwidth method, IWMBandwidthSharing.SetBandwidth, IWMBandwidthSharing::SetBandwidth, IWMBandwidthSharingSetBandwidth, SetBandwidth, SetBandwidth method [windows Media Format], SetBandwidth method [windows Media Format],IWMBandwidthSharing interface, wmformat.iwmbandwidthsharing_setbandwidth, wmsdkidl/IWMBandwidthSharing::SetBandwidth
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMBandwidthSharing.SetBandwidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMBandwidthSharing::SetBandwidth


## -description



The <b>SetBandwidth</b> method sets the bandwidth and maximum buffer size for a combined stream.




## -parameters




### -param dwBitrate [in]

<b>DWORD</b> containing the bit rate in bits per second. The combined bandwidths of the streams cannot exceed this value.


### -param msBufferWindow [in]

Specifies the buffer window in milliseconds. The combined buffer sizes of the streams cannot exceed this value.


## -returns



This method always returns S_OK.




## -remarks



The settings of a bandwidth sharing object are purely informational. They are not checked for accuracy.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743298(v=VS.85).aspx">IWMBandwidthSharing Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743299(v=VS.85).aspx">IWMBandwidthSharing::GetBandwidth</a>
 

 

