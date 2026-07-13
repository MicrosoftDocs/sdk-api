---
UID: NS:wingdi.DISPLAYCONFIG_PATH_INFO
title: DISPLAYCONFIG_PATH_INFO (wingdi.h)
description: The DISPLAYCONFIG_PATH_INFO structure is used to describe a single path from a target to a source.
helpviewer_keywords: ["CCD_Structures_2953f0bc-d985-40e0-894d-9fe2593061ed.xml","DISPLAYCONFIG_PATH_INFO","DISPLAYCONFIG_PATH_INFO structure [Display Devices]","display.displayconfig_path_info","wingdi/DISPLAYCONFIG_PATH_INFO"]
old-location: display\displayconfig_path_info.htm
tech.root: display
ms.assetid: e218c36d-60d5-42c8-9443-419a388a2b8d
ms.date: 12/05/2018
ms.keywords: CCD_Structures_2953f0bc-d985-40e0-894d-9fe2593061ed.xml, DISPLAYCONFIG_PATH_INFO, DISPLAYCONFIG_PATH_INFO structure [Display Devices], display.displayconfig_path_info, wingdi/DISPLAYCONFIG_PATH_INFO
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.typenames: DISPLAYCONFIG_PATH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_PATH_INFO
 - wingdi/DISPLAYCONFIG_PATH_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_PATH_INFO
---

# DISPLAYCONFIG_PATH_INFO structure


## -description

The DISPLAYCONFIG_PATH_INFO structure is used to describe a single path from a target to a source.

## -struct-fields

### -field sourceInfo

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a> structure that contains the source information for the path.

### -field targetInfo

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure that contains the target information for the path.

### -field flags

A bitwise OR of flag values that indicates the state of the path. The following values are supported:


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_PATH_ACTIVE"></a><a id="displayconfig_path_active"></a><dl>
<dt><b>DISPLAYCONFIG_PATH_ACTIVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set by <a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> to indicate that the path is active and part of the desktop. If this flag value is set, <a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> attempts to enable this path.
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE"></a><a id="displayconfig_path_support_virtual_mode"></a><dl>
<dt><b>DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<p>Set by <a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> to indicate that the path supports virtual modes. This flag is for reporting only and cannot be modified.</p>
<p>Supported starting in Windows 10.</p>
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_PATH_BOOST_REFRESH_RATE"></a><a id="displayconfig_path_boost_refresh_rate"></a><dl>
<dt><b>DISPLAYCONFIG_PATH_BOOST_REFRESH_RATE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
<p>Set by <a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> to indicate that the path is configured to automatically boost the refresh rate between the virtual refresh rate and the physical refresh rate (this is known as "Dynamic refresh rate"). This value can be set or removed for a path by <a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>. The virtual refresh rate is set by <a href="/windows/win32/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO.refreshRate</a> and the physical refresh rate is selected by <a href="/windows/win32/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE.targetVideoSignalInfo</a>.</p>
<p>Supported starting in Windows 11.</p>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>
