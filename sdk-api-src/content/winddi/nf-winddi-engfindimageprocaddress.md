---
UID: NF:winddi.EngFindImageProcAddress
title: EngFindImageProcAddress macro (winddi.h)
description: The EngFindImageProcAddress function returns the address of a function within an executable module.
helpviewer_keywords: ["EngFindImageProcAddress","EngFindImageProcAddress function [Display Devices]","display.engfindimageprocaddress","gdifncs_7680e4bd-d5d2-4365-84a0-131ea7a38b22.xml","winddi/EngFindImageProcAddress"]
old-location: display\engfindimageprocaddress.htm
tech.root: display
ms.assetid: a81c0814-3210-40dd-969f-20593353e54c
ms.date: 12/05/2018
ms.keywords: EngFindImageProcAddress, EngFindImageProcAddress function [Display Devices], display.engfindimageprocaddress, gdifncs_7680e4bd-d5d2-4365-84a0-131ea7a38b22.xml, winddi/EngFindImageProcAddress
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngFindImageProcAddress
 - winddi/EngFindImageProcAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngFindImageProcAddress
---

# EngFindImageProcAddress macro


## -description

The <b>EngFindImageProcAddress</b> function returns the address of a function within an executable module.

## -parameters

### -param h

Handle to the image in which the function can be found. This handle was obtained by calling <a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>. This parameter can be <b>NULL</b> on Windows NT 4.0 SP3 and later versions, which includes Windows 2000 and later operating system versions.

### -param procname [in]

Pointer to the string that specifies the name of the function to be located.

## -remarks

A driver must previously have loaded the image into kernel-mode through a call to <a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>.

The function identified by <i>lpProcName</i> must be exported by the loaded module. This is accomplished by using the EXPORTS key in the module's <i>.DEF</i> file.

A driver cannot call <b>EngFindImageProcAddress</b> with <i>hModule</i> set to <b>NULL</b> on any version of Windows NT 4.0 prior to SP3. Consequently, the driver must do version checking to ensure that the system is running that version or Windows 2000 or later. Specifically, if the <i>iEngineVersion</i> value passed to the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenabledriver">DrvEnableDriver</a> function is greater than or equal to DDI_DRIVER_VERSION_SP3, the driver can call <b>EngFindImageProcAddress</b> with a <b>NULL</b> value for <i>hModule</i>.

To obtain the address of a GDI service routine that is new to Windows 2000 and later operating system versions, the driver can call <b>EngFindImageProcAddress</b> with the function's string name and <i>hModule</i> set to <b>NULL</b>. The <i>lpProcName</i> parameter can be the text string equivalent of any of the following functions when <i>hModule</i> is <b>NULL</b>: 

<table>
<tr>
<td>
<b>BRUSHOBJ_hGetColorTransform</b>

</td>
<td>
<b>EngAlphaBlend</b>

</td>
</tr>
<tr>
<td>
<b>EngClearEvent</b>

</td>
<td>
<b>EngControlSprites</b>

</td>
</tr>
<tr>
<td>
<b>EngCreateEvent</b>

</td>
<td>
<b>EngDeleteEvent</b>

</td>
</tr>
<tr>
<td>
<b>EngDeleteFile</b>

</td>
<td>
<b>EngDeleteSafeSemaphore</b>

</td>
</tr>
<tr>
<td>
<b>EngDeleteWnd</b>

</td>
<td>
<b>EngDitherColor</b>

</td>
</tr>
<tr>
<td>
<b>EngGetPrinterDriver</b>

</td>
<td>
<b>EngGradientFill</b>

</td>
</tr>
<tr>
<td>
<b>EngHangNotification</b>

</td>
<td>
<b>EngInitializeSafeSemaphore</b>

</td>
</tr>
<tr>
<td>
<b>EngLockDirectDrawSurface</b>

</td>
<td>
<b>EngLpkInstalled</b>

</td>
</tr>
<tr>
<td>
<b>EngMapEvent</b>

</td>
<td>
<b>EngMapFile</b>

</td>
</tr>
<tr>
<td>
<b>EngMapFontFileFD</b>

</td>
<td>
<b>EngModifySurface</b>

</td>
</tr>
<tr>
<td>
<b>EngMovePointer</b>

</td>
<td>
<b>EngPlgBlt</b>

</td>
</tr>
<tr>
<td>
<b>EngQueryDeviceAttribute</b>

</td>
<td>
<b>EngQueryPalette</b>

</td>
</tr>
<tr>
<td>
<b>EngQuerySystemAttribute</b>

</td>
<td>
<b>EngReadStateEvent</b>

</td>
</tr>
<tr>
<td>
<b>EngRestoreFloatingPointState</b>

</td>
<td>
<b>EngSaveFloatingPointState</b>

</td>
</tr>
<tr>
<td>
<b>EngSetEvent</b>

</td>
<td>
<b>EngSetPointerShape</b>

</td>
</tr>
<tr>
<td>
<b>EngSetPointerTag</b>

</td>
<td>
<b>EngStretchBltROP</b>

</td>
</tr>
<tr>
<td>
<b>EngTransparentBlt</b>

</td>
<td>
<b>EngUnlockDirectDrawSurface</b>

</td>
</tr>
<tr>
<td>
<b>EngUnmapEvent</b>

</td>
<td>
<b>EngUnmapFile</b>

</td>
</tr>
<tr>
<td>
<b>EngUnmapFontFileFD</b>

</td>
<td>
<b>EngWaitForSingleObject</b>

</td>
</tr>
<tr>
<td>
<b>FONTOBJ_pfdg</b>

</td>
<td>
<b>FONTOBJ_pjOpenTypeTablePointer</b>

</td>
</tr>
<tr>
<td>
<b>FONTOBJ_pQueryGlyphAttrs</b>

</td>
<td>
<b>FONTOBJ_pwszFontFilePaths</b>

</td>
</tr>
<tr>
<td>
<b>HeapVidMemAllocAligned</b>

</td>
<td>
<b>HT_Get8BPPMaskPalette</b>

</td>
</tr>
<tr>
<td>
<b>STROBJ_bEnumPositionsOnly</b>

</td>
<td>
<b>STROBJ_bGetAdvanceWidths</b>

</td>
</tr>
<tr>
<td>
<b>STROBJ_fxBreakExtra</b>

</td>
<td>
<b>STROBJ_fxCharacterExtra</b>

</td>
</tr>
<tr>
<td>
<b>VidMemFree</b>

</td>
<td>
<b>XLATEOBJ_hGetColorTransform</b>

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledriver">DrvEnableDriver</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>