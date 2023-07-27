---
UID: NS:vmr9._VMR9MonitorInfo
title: VMR9MonitorInfo (vmr9.h)
description: The VMR9MonitorInfo structure is used with the VMR-9 in the IVMRMonitorConfig9::GetAvailableMonitors method to set and retrieve information about monitors on the system.
helpviewer_keywords: ["VMR9MonitorInfo","VMR9MonitorInfo structure [DirectShow]","VMR9MonitorInfoStructure","dshow.vmr9monitorinfo","vmr9/VMR9MonitorInfo"]
old-location: dshow\vmr9monitorinfo.htm
tech.root: dshow
ms.assetid: cb7d5c27-8762-450e-ba47-2a46e3106472
ms.date: 4/26/2023
ms.keywords: VMR9MonitorInfo, VMR9MonitorInfo structure [DirectShow], VMR9MonitorInfoStructure, dshow.vmr9monitorinfo, vmr9/VMR9MonitorInfo
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: VMR9MonitorInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9MonitorInfo
 - vmr9/_VMR9MonitorInfo
 - VMR9MonitorInfo
 - vmr9/VMR9MonitorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9MonitorInfo
---

# VMR9MonitorInfo structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9MonitorInfo</code> structure is used with the VMR-9 in the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmonitorconfig9-getavailablemonitors">IVMRMonitorConfig9::GetAvailableMonitors</a> method to set and retrieve information about monitors on the system.

## -struct-fields

### -field uDevID

Integer index that specifies the monitor device.

### -field rcMonitor

Specifies the monitor's rectangle.

### -field hMon

Handle to the monitor.

### -field dwFlags

Flags as defined for the <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a> structure. Currently the only valid flag is <b>MONITORINFOF_PRIMARY</b>, which indicates the primary display monitor.

### -field szDevice

Null-terminated string containing the device name.

### -field szDescription

Null-terminated string containing a description of the device.

### -field liDriverVersion

Specifies the driver version.

### -field dwVendorId

Specifies the vendor.

### -field dwDeviceId

Specifies the device ID.

### -field dwSubSysId

Specifies the device subsystem.

### -field dwRevision

Specifies the revision number.

## -remarks

This structure is used to configure monitors on multi-monitor systems.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>