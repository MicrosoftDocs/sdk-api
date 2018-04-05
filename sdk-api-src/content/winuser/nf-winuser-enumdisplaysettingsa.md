---
UID: NF:winuser.EnumDisplaySettingsA
title: EnumDisplaySettingsA function
author: windows-driver-content
description: The EnumDisplaySettings function retrieves information about one of the graphics modes for a display device. To retrieve information for all the graphics modes of a display device, make a series of calls to this function.
old-location: gdi\enumdisplaysettings.htm
old-project: gdi
ms.assetid: af73610b-bcd8-4660-800e-84fa0cc5b4eb
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ENUM_CURRENT_SETTINGS, ENUM_REGISTRY_SETTINGS, EnumDisplaySettings, EnumDisplaySettings function [Windows GDI], EnumDisplaySettingsA, EnumDisplaySettingsW, _win32_EnumDisplaySettings, gdi.enumdisplaysettings, winuser/EnumDisplaySettings, winuser/EnumDisplaySettingsA, winuser/EnumDisplaySettingsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDisplaySettingsW (Unicode) and EnumDisplaySettingsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
-	Ext-MS-Win-NTUser-sysparams-Ext-l1-1-0.dll
-	Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
-	minuser.dll
-	api-ms-win-ntuser-sysparams-l1-1-0.dll
api_name:
-	EnumDisplaySettings
-	EnumDisplaySettingsA
-	EnumDisplaySettingsW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumDisplaySettingsA function


## -description


The <b>EnumDisplaySettings</b> function retrieves information about one of the graphics modes for a display device. To retrieve information for all the graphics modes of a display device, make a series of calls to this function.
<div class="alert"><b>Note</b>  Apps that you design to target Windows 8 and later can no longer query or set display modes that are less than 32 bits per pixel (bpp); these operations will fail. These apps have a <a href="https://msdn.microsoft.com/f022374d-ea3f-477f-9b59-3188b775ed64">compatibility manifest</a> that targets Windows 8. Windows 8 still supports 8-bit and 16-bit color modes for desktop apps that were built without a Windows 8 manifest; Windows 8 emulates these modes but still runs in 32-bit color mode.</div><div> </div>

## -parameters




### -param lpszDeviceName [in]

A pointer to a null-terminated string that specifies the display device about whose graphics mode the function will obtain information.

This parameter is either <b>NULL</b> or a <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a>.<b>DeviceName</b> returned from <a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a>. A <b>NULL</b> value specifies the current display device on the computer on which the calling thread is running.


### -param iModeNum [in]

The type of information to be retrieved. This value can be a graphics mode index or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENUM_CURRENT_SETTINGS"></a><a id="enum_current_settings"></a><dl>
<dt><b>ENUM_CURRENT_SETTINGS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the current settings for the display device.

</td>
</tr>
<tr>
<td width="40%"><a id="ENUM_REGISTRY_SETTINGS"></a><a id="enum_registry_settings"></a><dl>
<dt><b>ENUM_REGISTRY_SETTINGS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the settings for the display device that are currently stored in the registry.

</td>
</tr>
</table>
 

Graphics mode indexes start at zero. To obtain information for all of a display device's graphics modes, make a series of calls to <b>EnumDisplaySettings</b>, as follows: Set <i>iModeNum</i> to zero for the first call, and increment <i>iModeNum</i> by one for each subsequent call. Continue calling the function until the return value is zero.

When you call <b>EnumDisplaySettings</b> with <i>iModeNum</i> set to zero, the operating system initializes and caches information about the display device. When you call <b>EnumDisplaySettings</b> with <i>iModeNum</i> set to a nonzero value, the function returns the information that was cached the last time the function was called with <i>iModeNum</i> set to zero.


### -param lpDevMode [out]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure into which the function stores information about the specified graphics mode. Before calling <b>EnumDisplaySettings</b>, set the <b>dmSize</b> member to <code>sizeof(DEVMODE)</code>, and set the <b>dmDriverExtra</b> member to indicate the size, in bytes, of the additional space available to receive private driver data.

The <b>EnumDisplaySettings</b> function sets values for the following five <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> members:

<ul>
<li><b>dmBitsPerPel</b></li>
<li><b>dmPelsWidth</b></li>
<li><b>dmPelsHeight</b></li>
<li><b>dmDisplayFlags</b></li>
<li><b>dmDisplayFrequency</b></li>
</ul>

## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The function fails if <i>iModeNum</i> is greater than the index of the display device's last graphics mode. As noted in the description of the <i>iModeNum</i> parameter, you can use this behavior to enumerate all of a display device's graphics modes.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output given is always in terms of physical pixels, and is not related to the calling context.




## -see-also




<a href="https://msdn.microsoft.com/208bf1cc-c03c-4d03-92e4-32fcf856b4d8">ChangeDisplaySettings</a>



<a href="https://msdn.microsoft.com/1448e04c-1452-4eab-bda4-4d249cb67a24">ChangeDisplaySettingsEx</a>



<a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>



<a href="base.createdesktop">CreateDesktop</a>



<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a>
 

 

