---
UID: NN:strmif.IVMRMonitorConfig
title: IVMRMonitorConfig (strmif.h)
description: The IVMRMonitorConfig interface is implemented by the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRMonitorConfig","IVMRMonitorConfig interface [DirectShow]","IVMRMonitorConfig interface [DirectShow]","described","IVMRMonitorConfigInterface","dshow.ivmrmonitorconfig","strmif/IVMRMonitorConfig"]
old-location: dshow\ivmrmonitorconfig.htm
tech.root: dshow
ms.assetid: 02b4016b-a65b-41ac-b5c6-e5f6825f179c
ms.date: 12/05/2018
ms.keywords: IVMRMonitorConfig, IVMRMonitorConfig interface [DirectShow], IVMRMonitorConfig interface [DirectShow],described, IVMRMonitorConfigInterface, dshow.ivmrmonitorconfig, strmif/IVMRMonitorConfig
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
 - IVMRMonitorConfig
 - strmif/IVMRMonitorConfig
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
 - IVMRMonitorConfig
---

# IVMRMonitorConfig interface


## -description

The <code>IVMRMonitorConfig</code> interface is implemented by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Applications use this interface to determine the capabilities of the display devices on the system and to control which device is used to display the output. For example, if the system contains a hardware DVD decoder and the VMR is rendering the output from that decoder, then on a multi-monitor system, an application must use this interface to specify the display device that is connected to the decoder.

The VMR-7 supports a maximum of 15 display devices.

It is the responsibility of the application to ensure that the playback window is positioned on the desired monitor before the window is displayed. Otherwise the playback window will be displayed at a location chosen by the Windows Shell (Explorer) which may not be on the desired monitor.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9">IVMRMonitorConfig9</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMonitorConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMonitorConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRMonitorConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getavailablemonitors">GetAvailableMonitors</a>
</td>
<td align="left" width="63%">
Retrieves information about the monitors currently available on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getdefaultmonitor">GetDefaultMonitor</a>
</td>
<td align="left" width="63%">
Retrieves the default monitor that all future instances of the VMR will use for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getmonitor">GetMonitor</a>
</td>
<td align="left" width="63%">
Retrieves the monitor that this instance of the VMR is using for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-setdefaultmonitor">SetDefaultMonitor</a>
</td>
<td align="left" width="63%">
Specifies the default monitor that all future instances of the VMR should use for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-setmonitor">SetMonitor</a>
</td>
<td align="left" width="63%">
On a multi-monitor system, specifies the monitor that this instance of the VMR should use for video playback.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>