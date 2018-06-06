---
UID: NF:wmsdkidl.IWMBandwidthSharing.GetBandwidth
title: IWMBandwidthSharing::GetBandwidth
author: windows-sdk-content
description: The GetBandwidth method retrieves the bandwidth and maximum buffer size of a combined stream.
old-location: wmformat\iwmbandwidthsharing_getbandwidth.htm
old-project: wmformat
ms.assetid: 2769328c-5c05-49fb-bfa6-729115dd417e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetBandwidth, GetBandwidth method [windows Media Format], GetBandwidth method [windows Media Format],IWMBandwidthSharing interface, IWMBandwidthSharing interface [windows Media Format],GetBandwidth method, IWMBandwidthSharing.GetBandwidth, IWMBandwidthSharing::GetBandwidth, IWMBandwidthSharingGetBandwidth, wmformat.iwmbandwidthsharing_getbandwidth, wmsdkidl/IWMBandwidthSharing::GetBandwidth
ms.prod: windows
ms.technology: windows-sdk
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
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMBandwidthSharing.GetBandwidth
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMBandwidthSharing::GetBandwidth


## -description



The <b>GetBandwidth</b> method retrieves the bandwidth and maximum buffer size of a combined stream.




## -parameters




### -param pdwBitrate [out]

Pointer to a <b>DWORD</b> containing the bit rate in bits per second. The combined bandwidths of the streams cannot exceed this value.


### -param pmsBufferWindow [out]

Pointer to <b>DWORD</b> containing the buffer window in milliseconds. The combined buffer sizes of the streams cannot exceed this value.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both of the parameters are <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The settings of a bandwidth sharing object are purely informational. They are not checked for accuracy.




## -see-also




<a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing Interface</a>



<a href="https://msdn.microsoft.com/1f2ac613-3674-46d9-ae7c-26389dbede02">IWMBandwidthSharing::SetBandwidth</a>
 

 

