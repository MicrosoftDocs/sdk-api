---
UID: NF:strmif.IVMRMonitorConfig.GetAvailableMonitors
title: IVMRMonitorConfig::GetAvailableMonitors (strmif.h)
description: The GetAvailableMonitors method retrieves information about the monitors currently available on the system.
helpviewer_keywords: ["GetAvailableMonitors","GetAvailableMonitors method [DirectShow]","GetAvailableMonitors method [DirectShow]","IVMRMonitorConfig interface","IVMRMonitorConfig interface [DirectShow]","GetAvailableMonitors method","IVMRMonitorConfig.GetAvailableMonitors","IVMRMonitorConfig::GetAvailableMonitors","IVMRMonitorConfigGetAvailableMonitors","dshow.ivmrmonitorconfig_getavailablemonitors","strmif/IVMRMonitorConfig::GetAvailableMonitors"]
old-location: dshow\ivmrmonitorconfig_getavailablemonitors.htm
tech.root: dshow
ms.assetid: 8a44ca7d-a195-4fcf-b09c-01f8176e0aa2
ms.date: 4/26/2023
ms.keywords: GetAvailableMonitors, GetAvailableMonitors method [DirectShow], GetAvailableMonitors method [DirectShow],IVMRMonitorConfig interface, IVMRMonitorConfig interface [DirectShow],GetAvailableMonitors method, IVMRMonitorConfig.GetAvailableMonitors, IVMRMonitorConfig::GetAvailableMonitors, IVMRMonitorConfigGetAvailableMonitors, dshow.ivmrmonitorconfig_getavailablemonitors, strmif/IVMRMonitorConfig::GetAvailableMonitors
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRMonitorConfig::GetAvailableMonitors
 - strmif/IVMRMonitorConfig::GetAvailableMonitors
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
 - IVMRMonitorConfig.GetAvailableMonitors
---

# IVMRMonitorConfig::GetAvailableMonitors


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAvailableMonitors</code> method retrieves information about the monitors currently available on the system.

## -parameters

### -param pInfo [out]

Pointer to an array of [VMRMONITORINFO](/windows/desktop/api/strmif/ns-strmif-vmrmonitorinfo) structures that contain information about each monitor on the system.

### -param dwMaxInfoArraySize [in]

Specifies the maximum number of members in the array.

### -param pdwNumDevices [out]

Pointer to a variable that receives the number of devices retrieved.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
</table>

## -remarks

Use this method to get a list of DirectDraw device GUIDs and their associated monitor information that the VMR can use when connecting to an upstream decoder filter. To return the required array size in the <i>pdwNumDevices</i> parameter, specify <b>NULL</b> for <i>pInfo</i>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmonitorconfig">IVMRMonitorConfig Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>