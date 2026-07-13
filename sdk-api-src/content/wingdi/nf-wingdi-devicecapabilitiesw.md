---
UID: NF:wingdi.DeviceCapabilitiesW
title: DeviceCapabilitiesW function (wingdi.h)
description: The DeviceCapabilities function retrieves the capabilities of a printer driver. (Unicode)
helpviewer_keywords: ["DC_BINNAMES", "DC_BINS", "DC_COLLATE", "DC_COLORDEVICE", "DC_COPIES", "DC_DRIVER", "DC_DUPLEX", "DC_ENUMRESOLUTIONS", "DC_EXTRA", "DC_FIELDS", "DC_FILEDEPENDENCIES", "DC_MAXEXTENT", "DC_MEDIAREADY", "DC_MEDIATYPENAMES", "DC_MEDIATYPES", "DC_MINEXTENT", "DC_NUP", "DC_ORIENTATION", "DC_PAPERNAMES", "DC_PAPERS", "DC_PAPERSIZE", "DC_PERSONALITY", "DC_PRINTERMEM", "DC_PRINTRATE", "DC_PRINTRATEPPM", "DC_PRINTRATEUNIT", "DC_SIZE", "DC_STAPLE", "DC_TRUETYPE", "DC_VERSION", "DeviceCapabilities", "DeviceCapabilities function [Windows GDI]", "DeviceCapabilitiesW", "_win32_DeviceCapabilities", "gdi.devicecapabilities", "wingdi/DeviceCapabilities", "wingdi/DeviceCapabilitiesW"]
old-location: gdi\devicecapabilities.htm
tech.root: xps
ms.assetid: d7f63ef7-0a2e-47c3-9e81-6e8a6dffe9af
ms.date: 12/05/2018
ms.keywords: DC_BINNAMES, DC_BINS, DC_COLLATE, DC_COLORDEVICE, DC_COPIES, DC_DRIVER, DC_DUPLEX, DC_ENUMRESOLUTIONS, DC_EXTRA, DC_FIELDS, DC_FILEDEPENDENCIES, DC_MAXEXTENT, DC_MEDIAREADY, DC_MEDIATYPENAMES, DC_MEDIATYPES, DC_MINEXTENT, DC_NUP, DC_ORIENTATION, DC_PAPERNAMES, DC_PAPERS, DC_PAPERSIZE, DC_PERSONALITY, DC_PRINTERMEM, DC_PRINTRATE, DC_PRINTRATEPPM, DC_PRINTRATEUNIT, DC_SIZE, DC_STAPLE, DC_TRUETYPE, DC_VERSION, DeviceCapabilities, DeviceCapabilities function [Windows GDI], DeviceCapabilitiesA, DeviceCapabilitiesW, _win32_DeviceCapabilities, gdi.devicecapabilities, wingdi/DeviceCapabilities, wingdi/DeviceCapabilitiesA, wingdi/DeviceCapabilitiesW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeviceCapabilitiesW (Unicode) and DeviceCapabilitiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinSpool.lib
req.dll: WinSpool.drv
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeviceCapabilitiesW
 - wingdi/DeviceCapabilitiesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-printer-winspool-l1-1-4.dll
 - ext-ms-win-printer-winspool-core-l1-1-0.dll
 - WinSpool.drv
 - Ext-MS-Win-printer-WinSpool-l1-1-2.dll
 - WinSpool.drv
 - Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
 - DeviceCapabilities
 - DeviceCapabilitiesA
 - DeviceCapabilitiesW
---

# DeviceCapabilitiesW function


## -description

The <b>DeviceCapabilities</b> function retrieves the capabilities of a printer driver.

## -parameters

### -param pDevice [in]

A pointer to a null-terminated string that contains the name of the printer. Note that this is the name of the printer, not of the printer driver.

### -param pPort [in]

A pointer to a null-terminated string that contains the name of the port to which the device is connected, such as LPT1.

### -param fwCapability [in]

The capabilities to be queried. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DC_BINNAMES"></a><a id="dc_binnames"></a><dl>
<dt><b>DC_BINNAMES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the names of the printer's paper bins. The <i>pOutput</i> buffer receives an array of string buffers. Each string buffer is 24 characters long and contains the name of a paper bin. The return value indicates the number of entries in the array. The name strings are null-terminated unless the name is 24 characters long. If <i>pOutput</i> is <b>NULL</b>, the return value is the number of bin entries required.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_BINS"></a><a id="dc_bins"></a><dl>
<dt><b>DC_BINS</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a list of available paper bins. The <i>pOutput</i> buffer receives an array of <b>WORD</b> values that indicate the available paper sources for the printer. The return value indicates the number of entries in the array. For a list of the possible array values, see the description of the <b>dmDefaultSource</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. If <i>pOutput</i> is <b>NULL</b>, the return value indicates the required number of entries in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_COLLATE"></a><a id="dc_collate"></a><dl>
<dt><b>DC_COLLATE</b></dt>
</dl>
</td>
<td width="60%">
If the printer supports collating, the return value is 1; otherwise, the return value is zero. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_COLORDEVICE"></a><a id="dc_colordevice"></a><dl>
<dt><b>DC_COLORDEVICE</b></dt>
</dl>
</td>
<td width="60%">
If the printer supports color printing, the return value is 1; otherwise, the return value is zero. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_COPIES"></a><a id="dc_copies"></a><dl>
<dt><b>DC_COPIES</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of copies the device can print.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_DRIVER"></a><a id="dc_driver"></a><dl>
<dt><b>DC_DRIVER</b></dt>
</dl>
</td>
<td width="60%">
Returns the version number of the printer driver.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_DUPLEX"></a><a id="dc_duplex"></a><dl>
<dt><b>DC_DUPLEX</b></dt>
</dl>
</td>
<td width="60%">
If the printer supports duplex printing, the return value is 1; otherwise, the return value is zero. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_ENUMRESOLUTIONS"></a><a id="dc_enumresolutions"></a><dl>
<dt><b>DC_ENUMRESOLUTIONS</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a list of the resolutions supported by the printer. The <i>pOutput</i> buffer receives an array of <b>LONG</b> values. For each supported resolution, the array contains a pair of <b>LONG</b> values that specify the x and y dimensions of the resolution, in dots per inch. The return value indicates the number of supported resolutions. If <i>pOutput</i> is <b>NULL</b>, the return value indicates the number of supported resolutions.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_EXTRA"></a><a id="dc_extra"></a><dl>
<dt><b>DC_EXTRA</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of bytes required for the device-specific portion of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure for the printer driver.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_FIELDS"></a><a id="dc_fields"></a><dl>
<dt><b>DC_FIELDS</b></dt>
</dl>
</td>
<td width="60%">
Returns the <b>dmFields</b> member of the printer driver's <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. The <b>dmFields</b> member indicates which members in the device-independent portion of the structure are supported by the printer driver.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_FILEDEPENDENCIES"></a><a id="dc_filedependencies"></a><dl>
<dt><b>DC_FILEDEPENDENCIES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the names of any additional files that need to be loaded when a driver is installed. The <i>pOutput</i> buffer receives an array of string buffers. Each string buffer is 64 characters long and contains the name of a file. The return value indicates the number of entries in the array. The name strings are null-terminated unless the name is 64 characters long. If <i>pOutput</i> is <b>NULL</b>, the return value is the number of files.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_MAXEXTENT"></a><a id="dc_maxextent"></a><dl>
<dt><b>DC_MAXEXTENT</b></dt>
</dl>
</td>
<td width="60%">
Returns the maximum paper size that the <b>dmPaperLength</b> and <b>dmPaperWidth</b> members of the printer driver's <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure can specify. The LOWORD of the return value contains the maximum <b>dmPaperWidth</b> value, and the HIWORD contains the maximum <b>dmPaperLength</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_MEDIAREADY"></a><a id="dc_mediaready"></a><dl>
<dt><b>DC_MEDIAREADY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the names of the paper forms that are currently available for use. The <i>pOutput</i> buffer receives an array of string buffers. Each string buffer is 64 characters long and contains the name of a paper form. The return value indicates the number of entries in the array. The name strings are null-terminated unless the name is 64 characters long. If <i>pOutput</i> is <b>NULL</b>, the return value is the number of paper forms.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_MEDIATYPENAMES"></a><a id="dc_mediatypenames"></a><dl>
<dt><b>DC_MEDIATYPENAMES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the names of the supported media types. The <i>pOutput</i> buffer receives an array of string buffers. Each string buffer is 64 characters long and contains the name of a supported media type. The return value indicates the number of entries in the array. The strings are null-terminated unless the name is 64 characters long. If <i>pOutput</i> is <b>NULL</b>, the return value is the number of media type names required.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_MEDIATYPES"></a><a id="dc_mediatypes"></a><dl>
<dt><b>DC_MEDIATYPES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a list of supported media types. The <i>pOutput</i> buffer receives an array of DWORD values that indicate the supported media types. The return value indicates the number of entries in the array. For a list of possible array values, see the description of the <b>dmMediaType</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. If <i>pOutput</i> is <b>NULL</b>, the return value indicates the required number of entries in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_MINEXTENT"></a><a id="dc_minextent"></a><dl>
<dt><b>DC_MINEXTENT</b></dt>
</dl>
</td>
<td width="60%">
Returns the minimum paper size that the <b>dmPaperLength</b> and <b>dmPaperWidth</b> members of the printer driver's <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure can specify. The LOWORD of the return value contains the minimum <b>dmPaperWidth</b> value, and the HIWORD contains the minimum <b>dmPaperLength</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_ORIENTATION"></a><a id="dc_orientation"></a><dl>
<dt><b>DC_ORIENTATION</b></dt>
</dl>
</td>
<td width="60%">
Returns the relationship between portrait and landscape orientations for a device, in terms of the number of degrees that portrait orientation is rotated counterclockwise to produce landscape orientation. The return value can be one of the following:

<dl>
<dt>0</dt>
<dd>
No landscape orientation.

</dd>
<dt>90</dt>
<dd>
Portrait is rotated 90 degrees to produce landscape.

</dd>
<dt>270</dt>
<dd>
Portrait is rotated 270 degrees to produce landscape.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="DC_NUP"></a><a id="dc_nup"></a><dl>
<dt><b>DC_NUP</b></dt>
</dl>
</td>
<td width="60%">
Retrieves an array of integers that indicate that printer's ability to print multiple document pages per printed page. The <i>pOutput</i> buffer receives an array of <b>DWORD</b> values. Each value represents a supported number of document pages per printed page. The return value indicates the number of entries in the array. If <i>pOutput</i> is <b>NULL</b>, the return value indicates the required number of entries in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PAPERNAMES"></a><a id="dc_papernames"></a><dl>
<dt><b>DC_PAPERNAMES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a list of supported paper names (for example, Letter or Legal). The <i>pOutput</i> buffer receives an array of string buffers. Each string buffer is 64 characters long and contains the name of a paper form. The return value indicates the number of entries in the array. The name strings are null-terminated unless the name is 64 characters long. If <i>pOutput</i> is <b>NULL</b>, the return value is the number of paper forms.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PAPERS"></a><a id="dc_papers"></a><dl>
<dt><b>DC_PAPERS</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a list of supported paper sizes. The <i>pOutput</i> buffer receives an array of <b>WORD</b> values that indicate the available paper sizes for the printer. The return value indicates the number of entries in the array. For a list of the possible array values, see the description of the <b>dmPaperSize</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. If <i>pOutput</i> is <b>NULL</b>, the return value indicates the required number of entries in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PAPERSIZE"></a><a id="dc_papersize"></a><dl>
<dt><b>DC_PAPERSIZE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the dimensions, in tenths of a millimeter, of each supported paper size. The <i>pOutput</i> buffer receives an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures. Each structure contains the width (x-dimension) and length (y-dimension) of a paper size as if the paper were in the <b>DMORIENT_PORTRAIT</b> orientation. The return value indicates the number of entries in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PERSONALITY"></a><a id="dc_personality"></a><dl>
<dt><b>DC_PERSONALITY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a list of printer description languages supported by the printer. The <i>pOutput</i> buffer receives an array of string buffers. Each buffer is 32 characters long and contains the name of a printer description language. The return value indicates the number of entries in the array. The name strings are null-terminated unless the name is 32 characters long. If <i>pOutput</i> is <b>NULL</b>, the return value indicates the required number of array entries.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PRINTERMEM"></a><a id="dc_printermem"></a><dl>
<dt><b>DC_PRINTERMEM</b></dt>
</dl>
</td>
<td width="60%">
The return value is the amount of available printer memory, in kilobytes. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PRINTRATE"></a><a id="dc_printrate"></a><dl>
<dt><b>DC_PRINTRATE</b></dt>
</dl>
</td>
<td width="60%">
The return value indicates the printer's print rate. The value returned for <b>DC_PRINTRATEUNIT</b> indicates the units of the <b>DC_PRINTRATE</b> value. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PRINTRATEPPM"></a><a id="dc_printrateppm"></a><dl>
<dt><b>DC_PRINTRATEPPM</b></dt>
</dl>
</td>
<td width="60%">
The return value indicates the printer's print rate, in pages per minute. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PRINTRATEUNIT"></a><a id="dc_printrateunit"></a><dl>
<dt><b>DC_PRINTRATEUNIT</b></dt>
</dl>
</td>
<td width="60%">
The return value is one of the following values that indicate the print rate units for the value returned for the <b>DC_PRINTRATE</b> flag. The <i>pOutput</i> parameter is not used.

<dl>
<dt><b>PRINTRATEUNIT_CPS</b></dt>
<dd>
Characters per second.

</dd>
<dt><b>PRINTRATEUNIT_IPM</b></dt>
<dd>
Inches per minute.

</dd>
<dt><b>PRINTRATEUNIT_LPM</b></dt>
<dd>
Lines per minute.

</dd>
<dt><b>PRINTRATEUNIT_PPM</b></dt>
<dd>
Pages per minute.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="DC_SIZE"></a><a id="dc_size"></a><dl>
<dt><b>DC_SIZE</b></dt>
</dl>
</td>
<td width="60%">
Returns the <b>dmSize</b> member of the printer driver's <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_STAPLE"></a><a id="dc_staple"></a><dl>
<dt><b>DC_STAPLE</b></dt>
</dl>
</td>
<td width="60%">
If the printer supports stapling, the return value is a nonzero value; otherwise, the return value is zero. The <i>pOutput</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_TRUETYPE"></a><a id="dc_truetype"></a><dl>
<dt><b>DC_TRUETYPE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the abilities of the driver to use TrueType fonts. For <b>DC_TRUETYPE</b>, the <i>pOutput</i> parameter should be <b>NULL</b>. The return value can be one or more of the following:

<dl>
<dt><b>DCTT_BITMAP</b></dt>
<dd>
Device can print TrueType fonts as graphics.

</dd>
<dt><b>DCTT_DOWNLOAD</b></dt>
<dd>
Device can download TrueType fonts.

</dd>
<dt><b>DCTT_SUBDEV</b></dt>
<dd>
Device can substitute device fonts for TrueType fonts.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="DC_VERSION"></a><a id="dc_version"></a><dl>
<dt><b>DC_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Returns the specification version to which the printer driver conforms.

</td>
</tr>
</table>

### -param pOutput [out]

A pointer to an array. The format of the array depends on the setting of the <i>fwCapability</i> parameter. See each capability above to find out what is returned if <i>pOutput</i> is <b>NULL</b>.

### -param pDevMode [in]

A pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. If this parameter is <b>NULL</b>, <b>DeviceCapabilities</b> retrieves the current default initialization values for the specified printer driver. Otherwise, the function retrieves the values contained in the structure to which <i>pDevMode</i> points.

## -returns

If the function succeeds, the return value depends on the setting of the <i>fwCapability</i> parameter. A return value of zero generally indicates that, while the function completed successfully, there was some type of failure, such as a capability that is not supported. For more details, see the descriptions for the <i>fwCapability</i> values.

If the function returns -1, this may mean either that the capability is not supported or there was a general function failure.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure pointed to by the <i>pDevMode</i> parameter may be obtained by calling the <a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a> function.

If a printer driver supports custom device capabilities, the driver must call the <a href="/windows/desktop/printdocs/setprinterdata">SetPrinterData</a> function for each custom capability. The <b>SetPrinterData</b> function adds the appropriate printer data to the print system, which enables 32-bit applications to access the custom capabilities on 64-bit Windows installations.

For each custom capability, you must first add printer data that describes the type of the capability. To do this, when you call <b>SetPrinterData</b>, set the <i>pValueName</i> string to <b>CustomDeviceCapabilityType_Xxx</b>, where "Xxx" is the hexadecimal representation of the capability. For example, you might have "CustomDeviceCapabilityType_1234". The registry data that you set must be of the <b>REG_DWORD</b> type, and you must set its value to one of the following:

<ul>
<li>0, if the custom capability is a <b>DWORD</b></li>
<li>1, if the custom capability is a buffer of bytes</li>
<li>2, if the custom capability is an array of items</li>
</ul>
If the custom capability is an array of items, you must call <b>SetPinterData</b> a second time to provide information about the size of an item in the array. To do this, when you call <b>SetPinterData</b>, the <i>pValueName</i> string that you provide must be "CustomDeviceCapabilitySize_Xxx" where Xxx is the hexadecimal representation of the capability. For example, you might have "CustomDeviceCapabilitySize_1234". The registry data that you set must be of the <b>REG_DWORD</b> type, and you must set its value to the size in bytes of an item in the array.





> [!NOTE]
> The wingdi.h header defines DeviceCapabilities as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-docinfoa">DOCINFO</a>



<a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a>
