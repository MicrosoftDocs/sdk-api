---
UID: NF:vmr9.IVMRMonitorConfig9.GetAvailableMonitors
title: IVMRMonitorConfig9::GetAvailableMonitors (vmr9.h)
description: The GetAvailableMonitors method retrieves information about the monitors currently available on the system.
helpviewer_keywords: ["GetAvailableMonitors","GetAvailableMonitors method [DirectShow]","GetAvailableMonitors method [DirectShow]","IVMRMonitorConfig9 interface","IVMRMonitorConfig9 interface [DirectShow]","GetAvailableMonitors method","IVMRMonitorConfig9.GetAvailableMonitors","IVMRMonitorConfig9::GetAvailableMonitors","IVMRMonitorConfig9GetAvailableMonitors","dshow.ivmrmonitorconfig9_getavailablemonitors","vmr9/IVMRMonitorConfig9::GetAvailableMonitors"]
old-location: dshow\ivmrmonitorconfig9_getavailablemonitors.htm
tech.root: dshow
ms.assetid: cebd40c2-ea41-4ed1-87d1-37f9d427c539
ms.date: 4/26/2023
ms.keywords: GetAvailableMonitors, GetAvailableMonitors method [DirectShow], GetAvailableMonitors method [DirectShow],IVMRMonitorConfig9 interface, IVMRMonitorConfig9 interface [DirectShow],GetAvailableMonitors method, IVMRMonitorConfig9.GetAvailableMonitors, IVMRMonitorConfig9::GetAvailableMonitors, IVMRMonitorConfig9GetAvailableMonitors, dshow.ivmrmonitorconfig9_getavailablemonitors, vmr9/IVMRMonitorConfig9::GetAvailableMonitors
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
 - IVMRMonitorConfig9::GetAvailableMonitors
 - vmr9/IVMRMonitorConfig9::GetAvailableMonitors
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
 - IVMRMonitorConfig9.GetAvailableMonitors
---

# IVMRMonitorConfig9::GetAvailableMonitors


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAvailableMonitors</code> method retrieves information about the monitors currently available on the system.

## -parameters

### -param pInfo [out]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9monitorinfo">VMR9MonitorInfo</a> structures that contain information about each monitor on the system.

### -param dwMaxInfoArraySize [in]

Specifies the maximum number of members in the array.

### -param pdwNumDevices [out]

If <i>pInfo</i> is <b>NULL</b>, this parameter receives the required array size. Otherwise, it receives the actual number of devices retrieved.

## -returns

The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>dwMaxInfoArraySize</i> must be greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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

Use this method to get a list of Direct Draw device identifiers and their associated monitor information that the mixer can use when connecting to an upstream decoder filter.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9">IVMRMonitorConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>