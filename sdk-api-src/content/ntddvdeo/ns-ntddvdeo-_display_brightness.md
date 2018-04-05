---
UID: NS:ntddvdeo._DISPLAY_BRIGHTNESS
title: "_DISPLAY_BRIGHTNESS"
author: windows-driver-content
description: Describes the brightness of the display device.
old-location: base\display_brightness.htm
old-project: Power
ms.assetid: 9edc7d30-496f-42a7-9865-45504d182f94
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PDISPLAY_BRIGHTNESS, DISPLAYPOLICY_AC, DISPLAYPOLICY_BOTH, DISPLAYPOLICY_DC, DISPLAY_BRIGHTNESS, DISPLAY_BRIGHTNESS structure, PDISPLAY_BRIGHTNESS, PDISPLAY_BRIGHTNESS structure pointer, _DISPLAY_BRIGHTNESS, base.display_brightness, ntddvdeo/DISPLAY_BRIGHTNESS, ntddvdeo/PDISPLAY_BRIGHTNESS, winnt/DISPLAY_BRIGHTNESS, winnt/PDISPLAY_BRIGHTNESS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddvdeo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
req.typenames: DISPLAY_BRIGHTNESS, *PDISPLAY_BRIGHTNESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
-	Ntddvdeo.h
api_name:
-	DISPLAY_BRIGHTNESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _DISPLAY_BRIGHTNESS structure


## -description


Describes the brightness of the display device. This structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567822">IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff568140">IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS</a> control codes. 


## -struct-fields




### -field ucDisplayPolicy

The display policy. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISPLAYPOLICY_AC"></a><a id="displaypolicy_ac"></a><dl>
<dt><b>DISPLAYPOLICY_AC</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
 AC power.

</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYPOLICY_DC"></a><a id="displaypolicy_dc"></a><dl>
<dt><b>DISPLAYPOLICY_DC</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
DC power.

</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYPOLICY_BOTH"></a><a id="displaypolicy_both"></a><dl>
<dt><b>DISPLAYPOLICY_BOTH</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Both AC and DC power. This value is valid only with <a href="https://msdn.microsoft.com/library/windows/hardware/ff568140">IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS</a>.

</td>
</tr>
</table>
 


### -field ucACBrightness

The AC brightness level. This is a value between 0 and 100. The larger the value, the brighter the backlight under AC power.


### -field ucDCBrightness

The DC brightness level. This is a value between 0 and 100. The larger the value, the brighter the backlight under DC power.


## -remarks



When calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff567822">IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS</a>, the <i>ucDisplayPolicy</i> parameter indicates the current power source, either AC or DC. When calling  <a href="https://msdn.microsoft.com/library/windows/hardware/ff568140">IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS</a>, this parameter determines which brightness levels are set: AC, DC, or both.

The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).  For information on obtaining the DDK, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84136">http://www.microsoft.com/whdc/devtools/ddk/default.mspx</a>.




## -see-also




<a href="https://msdn.microsoft.com/edf2b7ed-2676-483a-80ba-f148951e0e58">Backlight Control Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567822">IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568140">IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS</a>
 

 

