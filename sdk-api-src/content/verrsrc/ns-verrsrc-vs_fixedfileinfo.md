---
UID: NS:verrsrc.tagVS_FIXEDFILEINFO
title: VS_FIXEDFILEINFO (verrsrc.h)
description: Contains version information for a file. This information is language and code page independent.
helpviewer_keywords: ["VFT2_DRV_COMM","VFT2_DRV_DISPLAY","VFT2_DRV_INSTALLABLE","VFT2_DRV_KEYBOARD","VFT2_DRV_LANGUAGE","VFT2_DRV_MOUSE","VFT2_DRV_NETWORK","VFT2_DRV_PRINTER","VFT2_DRV_SOUND","VFT2_DRV_SYSTEM","VFT2_DRV_VERSIONED_PRINTER","VFT2_FONT_RASTER","VFT2_FONT_TRUETYPE","VFT2_FONT_VECTOR","VFT2_UNKNOWN","VFT_APP","VFT_DLL","VFT_DRV","VFT_FONT","VFT_STATIC_LIB","VFT_UNKNOWN","VFT_VXD","VOS_DOS","VOS_DOS_WINDOWS16","VOS_DOS_WINDOWS32","VOS_NT","VOS_NT_WINDOWS32","VOS_OS216","VOS_OS216_PM16","VOS_OS232","VOS_OS232_PM32","VOS_UNKNOWN","VOS__PM16","VOS__PM32","VOS__WINDOWS16","VOS__WINDOWS32","VS_FF_DEBUG","VS_FF_INFOINFERRED","VS_FF_PATCHED","VS_FF_PRERELEASE","VS_FF_PRIVATEBUILD","VS_FF_SPECIALBUILD","VS_FIXEDFILEINFO","VS_FIXEDFILEINFO structure [Menus and Other Resources]","_win32_VS_FIXEDFILEINFO_str","_win32_vs_fixedfileinfo_str_cpp","menurc.vs_fixedfileinfo","verrsrc/VS_FIXEDFILEINFO","winui._win32_vs_fixedfileinfo_str"]
old-location: menurc\vs_fixedfileinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationstructures\vs_fixedfileinfo.htm
ms.date: 12/05/2018
ms.keywords: VFT2_DRV_COMM, VFT2_DRV_DISPLAY, VFT2_DRV_INSTALLABLE, VFT2_DRV_KEYBOARD, VFT2_DRV_LANGUAGE, VFT2_DRV_MOUSE, VFT2_DRV_NETWORK, VFT2_DRV_PRINTER, VFT2_DRV_SOUND, VFT2_DRV_SYSTEM, VFT2_DRV_VERSIONED_PRINTER, VFT2_FONT_RASTER, VFT2_FONT_TRUETYPE, VFT2_FONT_VECTOR, VFT2_UNKNOWN, VFT_APP, VFT_DLL, VFT_DRV, VFT_FONT, VFT_STATIC_LIB, VFT_UNKNOWN, VFT_VXD, VOS_DOS, VOS_DOS_WINDOWS16, VOS_DOS_WINDOWS32, VOS_NT, VOS_NT_WINDOWS32, VOS_OS216, VOS_OS216_PM16, VOS_OS232, VOS_OS232_PM32, VOS_UNKNOWN, VOS__PM16, VOS__PM32, VOS__WINDOWS16, VOS__WINDOWS32, VS_FF_DEBUG, VS_FF_INFOINFERRED, VS_FF_PATCHED, VS_FF_PRERELEASE, VS_FF_PRIVATEBUILD, VS_FF_SPECIALBUILD, VS_FIXEDFILEINFO, VS_FIXEDFILEINFO structure [Menus and Other Resources], _win32_VS_FIXEDFILEINFO_str, _win32_vs_fixedfileinfo_str_cpp, menurc.vs_fixedfileinfo, verrsrc/VS_FIXEDFILEINFO, winui._win32_vs_fixedfileinfo_str
req.header: verrsrc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VS_FIXEDFILEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVS_FIXEDFILEINFO
 - verrsrc/tagVS_FIXEDFILEINFO
 - VS_FIXEDFILEINFO
 - verrsrc/VS_FIXEDFILEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VerRsrc.h
api_name:
 - VS_FIXEDFILEINFO
---

# VS_FIXEDFILEINFO structure


## -description

Contains version information for a file. This information is language and code page independent.

## -struct-fields

### -field dwSignature

Type: <b>DWORD</b>

Contains the value 0xFEEF04BD. This is used with the 
					<b>szKey</b> member of the <a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a> structure when searching a file for the <b>VS_FIXEDFILEINFO</b> structure.

### -field dwStrucVersion

Type: <b>DWORD</b>

The binary version number of this structure. The high-order word of this member contains the major version number, and the low-order word contains the minor version number.

### -field dwFileVersionMS

Type: <b>DWORD</b>

The most significant 32 bits of the file's binary version number. This member is used with 
					<b>dwFileVersionLS</b> to form a 64-bit value used for numeric comparisons.

### -field dwFileVersionLS

Type: <b>DWORD</b>

The least significant 32 bits of the file's binary version number. This member is used with 
					<b>dwFileVersionMS</b> to form a 64-bit value used for numeric comparisons.

### -field dwProductVersionMS

Type: <b>DWORD</b>

The most significant 32 bits of the binary version number of the product with which this file was distributed. This member is used with 
					<b>dwProductVersionLS</b> to form a 64-bit value used for numeric comparisons.

### -field dwProductVersionLS

Type: <b>DWORD</b>

The least significant 32 bits of the binary version number of the product with which this file was distributed. This member is used with 
					<b>dwProductVersionMS</b> to form a 64-bit value used for numeric comparisons.

### -field dwFileFlagsMask

Type: <b>DWORD</b>

Contains a bitmask that specifies the valid bits in 
					<b>dwFileFlags</b>. A bit is valid only if it was defined when the file was created.

### -field dwFileFlags

Type: <b>DWORD</b>

Contains a bitmask that specifies the Boolean attributes of the file. This member can include one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VS_FF_DEBUG"></a><a id="vs_ff_debug"></a><dl>
<dt><b>VS_FF_DEBUG</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The file contains debugging information or is compiled with debugging features enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="VS_FF_INFOINFERRED"></a><a id="vs_ff_infoinferred"></a><dl>
<dt><b>VS_FF_INFOINFERRED</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
The file's version structure was created dynamically; therefore, some of the members in this structure may be empty or incorrect. This flag should never be set in a file's <a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a> data.

</td>
</tr>
<tr>
<td width="40%"><a id="VS_FF_PATCHED"></a><a id="vs_ff_patched"></a><dl>
<dt><b>VS_FF_PATCHED</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
The file has been modified and is not identical to the original shipping file of the same version number.

</td>
</tr>
<tr>
<td width="40%"><a id="VS_FF_PRERELEASE"></a><a id="vs_ff_prerelease"></a><dl>
<dt><b>VS_FF_PRERELEASE</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The file is a development version, not a commercially released product.

</td>
</tr>
<tr>
<td width="40%"><a id="VS_FF_PRIVATEBUILD"></a><a id="vs_ff_privatebuild"></a><dl>
<dt><b>VS_FF_PRIVATEBUILD</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
The file was not built using standard release procedures. If this flag is set, the <a href="/windows/desktop/menurc/stringfileinfo">StringFileInfo</a> structure should contain a PrivateBuild entry.

</td>
</tr>
<tr>
<td width="40%"><a id="VS_FF_SPECIALBUILD"></a><a id="vs_ff_specialbuild"></a><dl>
<dt><b>VS_FF_SPECIALBUILD</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
The file was built by the original company using standard release procedures but is a variation of the normal file of the same version number. If this flag is set, the <a href="/windows/desktop/menurc/stringfileinfo">StringFileInfo</a> structure should contain a SpecialBuild entry.

</td>
</tr>
</table>

### -field dwFileOS

Type: <b>DWORD</b>

The operating system for which this file was designed. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VOS_DOS"></a><a id="vos_dos"></a><dl>
<dt><b>VOS_DOS</b></dt>
<dt>0x00010000L</dt>
</dl>
</td>
<td width="60%">
The file was designed for MS-DOS.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_NT"></a><a id="vos_nt"></a><dl>
<dt><b>VOS_NT</b></dt>
<dt>0x00040000L</dt>
</dl>
</td>
<td width="60%">
The file was designed for Windows NT.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS__WINDOWS16"></a><a id="vos__windows16"></a><dl>
<dt><b>VOS__WINDOWS16</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 16-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS__WINDOWS32"></a><a id="vos__windows32"></a><dl>
<dt><b>VOS__WINDOWS32</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 32-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_OS216"></a><a id="vos_os216"></a><dl>
<dt><b>VOS_OS216</b></dt>
<dt>0x00020000L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 16-bit OS/2.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_OS232"></a><a id="vos_os232"></a><dl>
<dt><b>VOS_OS232</b></dt>
<dt>0x00030000L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 32-bit OS/2.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS__PM16"></a><a id="vos__pm16"></a><dl>
<dt><b>VOS__PM16</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 16-bit Presentation Manager.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS__PM32"></a><a id="vos__pm32"></a><dl>
<dt><b>VOS__PM32</b></dt>
<dt>0x00000003L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 32-bit Presentation Manager.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_UNKNOWN"></a><a id="vos_unknown"></a><dl>
<dt><b>VOS_UNKNOWN</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operating system for which the file was designed is unknown to the system.

</td>
</tr>
</table>
 


An application can combine these values to indicate that the file was designed for one operating system running on another. The following 
					<b>dwFileOS</b> values are examples of this, but are not a complete list.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VOS_DOS_WINDOWS16"></a><a id="vos_dos_windows16"></a><dl>
<dt><b>VOS_DOS_WINDOWS16</b></dt>
<dt>0x00010001L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 16-bit Windows running on MS-DOS.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_DOS_WINDOWS32"></a><a id="vos_dos_windows32"></a><dl>
<dt><b>VOS_DOS_WINDOWS32</b></dt>
<dt>0x00010004L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 32-bit Windows running on MS-DOS.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_NT_WINDOWS32"></a><a id="vos_nt_windows32"></a><dl>
<dt><b>VOS_NT_WINDOWS32</b></dt>
<dt>0x00040004L</dt>
</dl>
</td>
<td width="60%">
The file was designed for Windows NT.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_OS216_PM16"></a><a id="vos_os216_pm16"></a><dl>
<dt><b>VOS_OS216_PM16</b></dt>
<dt>0x00020002L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 16-bit Presentation Manager running on 16-bit OS/2.

</td>
</tr>
<tr>
<td width="40%"><a id="VOS_OS232_PM32"></a><a id="vos_os232_pm32"></a><dl>
<dt><b>VOS_OS232_PM32</b></dt>
<dt>0x00030003L</dt>
</dl>
</td>
<td width="60%">
The file was designed for 32-bit Presentation Manager running on 32-bit OS/2.

</td>
</tr>
</table>

### -field dwFileType

Type: <b>DWORD</b>

The general type of file. This member can be one of the following values. All other values are reserved. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VFT_APP"></a><a id="vft_app"></a><dl>
<dt><b>VFT_APP</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The file contains an application.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT_DLL"></a><a id="vft_dll"></a><dl>
<dt><b>VFT_DLL</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The file contains a DLL.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT_DRV"></a><a id="vft_drv"></a><dl>
<dt><b>VFT_DRV</b></dt>
<dt>0x00000003L</dt>
</dl>
</td>
<td width="60%">
The file contains a device driver. If 
						<b>dwFileType</b> is <b>VFT_DRV</b>, 
						<b>dwFileSubtype</b> contains a more specific description of the driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT_FONT"></a><a id="vft_font"></a><dl>
<dt><b>VFT_FONT</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
The file contains a font. If 
						<b>dwFileType</b> is <b>VFT_FONT</b>, 
						<b>dwFileSubtype</b> contains a more specific description of the font file.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT_STATIC_LIB"></a><a id="vft_static_lib"></a><dl>
<dt><b>VFT_STATIC_LIB</b></dt>
<dt>0x00000007L</dt>
</dl>
</td>
<td width="60%">
The file contains a static-link library.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT_UNKNOWN"></a><a id="vft_unknown"></a><dl>
<dt><b>VFT_UNKNOWN</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The file type is unknown to the system.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT_VXD"></a><a id="vft_vxd"></a><dl>
<dt><b>VFT_VXD</b></dt>
<dt>0x00000005L</dt>
</dl>
</td>
<td width="60%">
The file contains a virtual device.

</td>
</tr>
</table>

### -field dwFileSubtype

Type: <b>DWORD</b>

The function of the file. The possible values depend on the value of 
					<b>dwFileType</b>. For all values of 
					<b>dwFileType</b> not described in the following list, 
					<b>dwFileSubtype</b> is zero. 


If 
						<b>dwFileType</b> is <b>VFT_DRV</b>, 
						<b>dwFileSubtype</b> can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_COMM"></a><a id="vft2_drv_comm"></a><dl>
<dt><b>VFT2_DRV_COMM</b></dt>
<dt>0x0000000AL</dt>
</dl>
</td>
<td width="60%">
The file contains a communications driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_DISPLAY"></a><a id="vft2_drv_display"></a><dl>
<dt><b>VFT2_DRV_DISPLAY</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
The file contains a display driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_INSTALLABLE"></a><a id="vft2_drv_installable"></a><dl>
<dt><b>VFT2_DRV_INSTALLABLE</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
The file contains an installable driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_KEYBOARD"></a><a id="vft2_drv_keyboard"></a><dl>
<dt><b>VFT2_DRV_KEYBOARD</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The file contains a keyboard driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_LANGUAGE"></a><a id="vft2_drv_language"></a><dl>
<dt><b>VFT2_DRV_LANGUAGE</b></dt>
<dt>0x00000003L</dt>
</dl>
</td>
<td width="60%">
The file contains a language driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_MOUSE"></a><a id="vft2_drv_mouse"></a><dl>
<dt><b>VFT2_DRV_MOUSE</b></dt>
<dt>0x00000005L</dt>
</dl>
</td>
<td width="60%">
The file contains a mouse driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_NETWORK"></a><a id="vft2_drv_network"></a><dl>
<dt><b>VFT2_DRV_NETWORK</b></dt>
<dt>0x00000006L</dt>
</dl>
</td>
<td width="60%">
The file contains a network driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_PRINTER"></a><a id="vft2_drv_printer"></a><dl>
<dt><b>VFT2_DRV_PRINTER</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The file contains a printer driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_SOUND"></a><a id="vft2_drv_sound"></a><dl>
<dt><b>VFT2_DRV_SOUND</b></dt>
<dt>0x00000009L</dt>
</dl>
</td>
<td width="60%">
The file contains a sound driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_SYSTEM"></a><a id="vft2_drv_system"></a><dl>
<dt><b>VFT2_DRV_SYSTEM</b></dt>
<dt>0x00000007L</dt>
</dl>
</td>
<td width="60%">
The file contains a system driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_DRV_VERSIONED_PRINTER"></a><a id="vft2_drv_versioned_printer"></a><dl>
<dt><b>VFT2_DRV_VERSIONED_PRINTER</b></dt>
<dt>0x0000000CL</dt>
</dl>
</td>
<td width="60%">
The file contains a versioned printer driver.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_UNKNOWN"></a><a id="vft2_unknown"></a><dl>
<dt><b>VFT2_UNKNOWN</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The driver type is unknown by the system.

</td>
</tr>
</table>
 


If 
						<b>dwFileType</b> is <b>VFT_FONT</b>, 
						<b>dwFileSubtype</b> can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VFT2_FONT_RASTER"></a><a id="vft2_font_raster"></a><dl>
<dt><b>VFT2_FONT_RASTER</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The file contains a raster font.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_FONT_TRUETYPE"></a><a id="vft2_font_truetype"></a><dl>
<dt><b>VFT2_FONT_TRUETYPE</b></dt>
<dt>0x00000003L</dt>
</dl>
</td>
<td width="60%">
The file contains a TrueType font.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_FONT_VECTOR"></a><a id="vft2_font_vector"></a><dl>
<dt><b>VFT2_FONT_VECTOR</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The file contains a vector font.

</td>
</tr>
<tr>
<td width="40%"><a id="VFT2_UNKNOWN"></a><a id="vft2_unknown"></a><dl>
<dt><b>VFT2_UNKNOWN</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The font type is unknown by the system.

</td>
</tr>
</table>
 

If 
						<b>dwFileType</b> is <b>VFT_VXD</b>, 
						<b>dwFileSubtype</b> contains the virtual device identifier included in the virtual device control block.

All 
						<b>dwFileSubtype</b> values not listed here are reserved.

### -field dwFileDateMS

Type: <b>DWORD</b>

The most significant 32 bits of the file's 64-bit binary creation date and time stamp.

This field is not used and should be zero.

### -field dwFileDateLS

Type: <b>DWORD</b>

The least significant 32 bits of the file's 64-bit binary creation date and time stamp.

This field is not used and should be zero.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/string-str">String</a>



<a href="/windows/desktop/menurc/stringfileinfo">StringFileInfo</a>



<a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
