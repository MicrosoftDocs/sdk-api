---
UID: NF:strmif.IVMRMonitorConfig.GetDefaultMonitor
title: IVMRMonitorConfig::GetDefaultMonitor (strmif.h)
description: The GetDefaultMonitor method retrieves the default monitor that all future instances of the VMR will use for video playback.
helpviewer_keywords: ["GetDefaultMonitor","GetDefaultMonitor method [DirectShow]","GetDefaultMonitor method [DirectShow]","IVMRMonitorConfig interface","IVMRMonitorConfig interface [DirectShow]","GetDefaultMonitor method","IVMRMonitorConfig.GetDefaultMonitor","IVMRMonitorConfig::GetDefaultMonitor","IVMRMonitorConfigGetDefaultMonitor","dshow.ivmrmonitorconfig_getdefaultmonitor","strmif/IVMRMonitorConfig::GetDefaultMonitor"]
old-location: dshow\ivmrmonitorconfig_getdefaultmonitor.htm
tech.root: dshow
ms.assetid: 354b7f6e-35f8-4824-b5b5-24a37166462b
ms.date: 4/26/2023
ms.keywords: GetDefaultMonitor, GetDefaultMonitor method [DirectShow], GetDefaultMonitor method [DirectShow],IVMRMonitorConfig interface, IVMRMonitorConfig interface [DirectShow],GetDefaultMonitor method, IVMRMonitorConfig.GetDefaultMonitor, IVMRMonitorConfig::GetDefaultMonitor, IVMRMonitorConfigGetDefaultMonitor, dshow.ivmrmonitorconfig_getdefaultmonitor, strmif/IVMRMonitorConfig::GetDefaultMonitor
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
 - IVMRMonitorConfig::GetDefaultMonitor
 - strmif/IVMRMonitorConfig::GetDefaultMonitor
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
 - IVMRMonitorConfig.GetDefaultMonitor
---

# IVMRMonitorConfig::GetDefaultMonitor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDefaultMonitor</code> method retrieves the default monitor that all future instances of the VMR will use for video playback.

## -parameters

### -param pGUID [out]

Pointer to a [VMRGUID](/windows/desktop/api/strmif/ns-strmif-vmrguid) structure that identifies the default monitor on the system.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The allocator-presenter has not been loaded.

</td>
</tr>
</table>

## -remarks

Use this method on a multi-monitor system to determine which is the default DirectDraw device the VMR will use when connecting to an upstream filter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmonitorconfig">IVMRMonitorConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-setdefaultmonitor">IVMRMonitorConfig::SetDefaultMonitor</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>