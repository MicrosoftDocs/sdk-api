---
UID: NS:wingdi._devicemodeW
title: DEVMODEW (wingdi.h)
description: The DEVMODEW structure is used for specifying characteristics of display and print devices in the Unicode (wide) character set.
helpviewer_keywords: ["*LPDEVMODEW","*NPDEVMODEW","*PDEVMODEW","DEVMODE","DEVMODEW","DEVMODEW structure [Display Devices]","LPDEVMODEW","LPDEVMODEW structure pointer [Display Devices]","NPDEVMODEW","NPDEVMODEW structure pointer [Display Devices]","PDEVMODEW","PDEVMODEW structure pointer [Display Devices]","display.devmodew","grstrcts_79d0f44a-67f8-432b-ad2c-a1a3ef18da95.xml","wingdi/DEVMODEW","wingdi/LPDEVMODEW","wingdi/NPDEVMODEW","wingdi/PDEVMODEW"]
old-location: display\devmodew.htm
tech.root: display
ms.assetid: b2369876-9a79-40c8-8d27-c8b9d8e68e6b
ms.date: 06/13/2023
ms.keywords: '*LPDEVMODEW, *NPDEVMODEW, *PDEVMODEW, DEVMODE, DEVMODEW, DEVMODEW structure [Display Devices], LPDEVMODEW, LPDEVMODEW structure pointer [Display Devices], NPDEVMODEW, NPDEVMODEW structure pointer [Display Devices], PDEVMODEW, PDEVMODEW structure pointer [Display Devices], display.devmodew, grstrcts_79d0f44a-67f8-432b-ad2c-a1a3ef18da95.xml, wingdi/DEVMODEW, wingdi/LPDEVMODEW, wingdi/NPDEVMODEW, wingdi/PDEVMODEW'
req.header: wingdi.h
req.include-header: Wingdi.h
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
req.typenames: DEVMODEW, *PDEVMODEW, *NPDEVMODEW, *LPDEVMODEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _devicemodeW
 - wingdi/_devicemodeW
 - PDEVMODEW
 - wingdi/PDEVMODEW
 - DEVMODEW
 - wingdi/DEVMODEW
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
 - DEVMODEW
---

## -description

The DEVMODEW structure is used for specifying characteristics of display and print devices in the Unicode (wide) character set.

## -struct-fields

### -field dmDeviceName

For a display, specifies the name of the display driver's DLL; for example, "perm3dd" for the 3Dlabs Permedia3 display driver.

For a printer, specifies the "friendly name"; for example, "PCL/HP LaserJet" in the case of PCL/HP LaserJet. If the name is greater than CCHDEVICENAME characters in length, the spooler truncates it to fit in the array.

### -field dmSpecVersion

Specifies the version number of this DEVMODEW structure. The current version number is identified by the DM_SPECVERSION constant in <i>wingdi.h</i>.

### -field dmDriverVersion

For a printer, specifies the printer driver version number assigned by the printer driver developer.

Display drivers can set this member to DM_SPECVERSION.

### -field dmSize

Specifies the size in bytes of the public DEVMODEW structure, not including any private, driver-specified members identified by the <b>dmDriverExtra</b> member.

### -field dmDriverExtra

Specifies the number of bytes of private driver data that follow the public structure members. If a device driver does not provide private DEVMODEW members, this member should be set to zero.

### -field dmFields

Specifies bit flags identifying which of the following DEVMODEW members are in use. For example, the DM_ORIENTATION flag is set when the <b>dmOrientation</b> member contains valid data. The DM_XXX flags are defined in <i>wingdi.h</i>.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmOrientation

For printers, specifies the paper orientation. This member can be either DMORIENT_PORTRAIT or DMORIENT_LANDSCAPE.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPaperSize

For printers, specifies the size of the paper to be printed on. This member must be zero if the length and width of the paper are specified by the <b>dmPaperLength</b> and <b>dmPaperWidth</b> members. Otherwise, the <b>dmPaperSize</b> member must be one of the DMPAPER-prefixed constants defined in <i>wingdi.h</i>.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPaperLength

For printers, specifies the length of the paper, in units of 1/10 of a millimeter. This value overrides the length of the paper specified by the <b>dmPaperSize</b> member, and is used if the paper is of a custom size, or if the device is a dot matrix printer, which can print a page of arbitrary length.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPaperWidth

For printers, specifies the width of the paper, in units of 1/10 of a millimeter. This value overrides the width of the paper specified by the <b>dmPaperSize</b> member. This member must be used if <b>dmPaperLength</b> is used.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmScale

For printers, specifies the percentage by which the image is to be scaled for printing. The image's page size is scaled to the physical page by a factor of <b>dmScale</b>/100. For example, a 17-inch by 22-inch image with a scale value of 100 requires 17x22-inch paper, while the same image with a scale value of 50 should print as half-sized and fit on letter-sized paper.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmCopies

For printers, specifies the number of copies to be printed, if the device supports multiple copies.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmDefaultSource

For printers, specifies the printer's default input bin. This must be one of the DMBIN-prefixed constants defined in <i>wingdi.h</i>. If the specified constant is DMBIN_FORMSOURCE, the input bin should be selected automatically.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPrintQuality

For printers, specifies the printer resolution. The following negative constant values are defined in <i>wingdi.h</i>:


<dl>
<dt>DMRES_HIGH</dt>
<dt>DMRES_MEDIUM</dt>
<dt>DMRES_LOW</dt>
<dt>DMRES_DRAFT</dt>
</dl>


If a positive value is specified, it represents the number of dots per inch (DPI) for the <i>x</i> resolution, and the <i>y</i> resolution is specified by <b>dmYResolution</b>.

This member is not used for displays.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2.dmPosition

For displays, specifies a <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structure containing the x- and y-coordinates of upper-left corner of the display, in desktop coordinates. This member is used to determine the relative position of monitors in a multiple monitor environment.

This member is not used for printers.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2.dmDisplayOrientation

This member is defined only for Windows XP and later. 

For displays, specifies the orientation at which images should be presented. When the DM_DISPLAYORIENTATION bit is not set in the <b>dmFields</b> member, this member must be set to zero. When the DM_DISPLAYORIENTATION bit is set in the <b>dmFields</b> member, this member must be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DMDO_DEFAULT

</td>
<td>
The current mode's display device orientation is the natural orientation of the device, and should be used as the default.

</td>
</tr>
<tr>
<td>
DMDO_90

</td>
<td>
The display device orientation is 90 degrees (measured counter-clockwise) from that of DMDO_DEFAULT.

</td>
</tr>
<tr>
<td>
DMDO_180

</td>
<td>
The display device orientation is 180 degrees (measured counter-clockwise) from that of DMDO_DEFAULT.

</td>
</tr>
<tr>
<td>
DMDO_270

</td>
<td>
The display device orientation is 270 degrees (measured counter-clockwise) from that of DMDO_DEFAULT.

</td>
</tr>
</table>
 

This member is not used for printers.

For more information, see <a href="/windows-hardware/drivers/display/returning-display-modes--drvgetmodes">Returning Display Modes: DrvGetModes</a>.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2.dmDisplayFixedOutput

This member is defined only for Windows XP and later. 

For fixed-resolution displays, specifies how the device can present a lower-resolution mode on a higher-resolution display. For example, if a display device's resolution is fixed at 1024 X 768, and its mode is set to 640 x 480, the device can either display a 640 X 480 image within the 1024 X 768 screen space, or stretch the 640 X 480 image to fill the larger screen space. 

When the DM_DISPLAYFIXEDOUTPUT bit is not set in the <b>dmFields</b> member, this member must be set to zero. When the DM_DISPLAYFIXEDOUTPUT bit is set in the <b>dmFields</b> member, this member must be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DMDFO_CENTER

</td>
<td>
The display device presents a lower resolution mode image by centering it in the larger screen space.

</td>
</tr>
<tr>
<td>
DMDFO_STRETCH

</td>
<td>
The display device presents a lower-resolution mode image by stretching it to fill the larger screen space.

</td>
</tr>
</table>
 

This member is not used for printers.

For more information, see <a href="/windows-hardware/drivers/display/returning-display-modes--drvgetmodes">Returning Display Modes: DrvGetModes</a>.

### -field dmColor

For printers, specifies whether a color printer should print color or monochrome. This member can be one of DMCOLOR_COLOR or DMCOLOR_MONOCHROME.

This member is not used for displays.

### -field dmDuplex

For printers, specifies duplex (double-sided) printing for duplex-capable printers. This member can be one of the following values:





#### DMDUP_HORIZONTAL

Print double-sided, using short edge binding.



#### DMDUP_SIMPLEX

Print single-sided.



#### DMDUP_VERTICAL

Print double-sided, using long edge binding.

This member is not used for displays.

### -field dmYResolution

For printers, specifies the <i>y</i> resolution of the printer, in DPI. If this member is used, the <b>dmPrintQuality</b> member specifies the <i>x</i> resolution.

This member is not used for displays.

### -field dmTTOption

For printers, specifies how TrueType fonts should be printed. This member must be one of the DMTT-prefixed constants defined in <i>wingdi.h</i>.

This member is not used for displays.

### -field dmCollate

For printers, specifies whether multiple copies should be collated. This member can be one of the following values:





#### DMCOLLATE_TRUE

Collate when printing multiple copies.



#### DMCOLLATE_FALSE

Do not collate when printing multiple copies.

This member is not used for displays.

### -field dmFormName

For printers, specifies the name of the form to use; such as "Letter" or "Legal". This must be a name that can be obtain by calling the Win32 <a href="/windows/win32/printdocs/enumforms">EnumForms</a> function.

This member is not used for displays.

### -field dmLogPixels

For displays, specifies the number of logical pixels per inch of a display device and should be equal to the <b>ulLogPixels</b> member of the <a href="/windows/win32/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure.

This member is not used for printers.

### -field dmBitsPerPel

For displays, specifies the color resolution, in bits per pixel, of a display device. 

This member is not used for printers.

### -field dmPelsWidth

For displays, specifies the width, in pixels, of the visible device surface.

This member is not used for printers.

### -field dmPelsHeight

For displays, specifies the height, in pixels, of the visible device surface. 

This member is not used for printers.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.dmDisplayFlags

Specifies the device's display mode. This member can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DM_GRAYSCALE</td>
<td>Specifies that the display is a noncolor device. If this flag is not set, color is assumed. This flag is no longer valid.</td>
</tr>
<tr>
<td>DM_INTERLACED</td>
<td>Specifies that the display mode is interlaced. If the flag is not set, noninterlaced is assumed.</td>
</tr>
</table>

Display drivers use this member; for example, in the [ChangeDisplaySettings](/windows/win32/api/winuser/nf-winuser-changedisplaysettingsa) function. Printer drivers don't use this member.

### -field DUMMYUNIONNAME2.dmNup

For printers, specifies whether the print system handles "N-up" printing (playing multiple EMF logical pages onto a single physical page). The value of this member can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DMNUP_SYSTEM

</td>
<td>
The print system handles "N-up" printing. 

</td>
</tr>
<tr>
<td>
DMNUP_ONEUP

</td>
<td>
The print system does not handle "N-up" printing. An application can set <b>dmNup</b> to DMNUP_ONEUP if it intends to carry out "N-up" printing on its own.

</td>
</tr>
</table>
 

This member is not used for displays.

### -field dmDisplayFrequency

For displays, specifies the frequency, in hertz, of a display device in its current mode.

This member is not used for printers.

### -field dmICMMethod

Specifies one of the DMICMMETHOD-prefixed constants defined in <i>wingdi.h</i>.

### -field dmICMIntent

Specifies one of the DMICM-prefixed constants defined in <i>wingdi.h</i>.

### -field dmMediaType

Specifies one of the DMMEDIA-prefixed constants defined in <i>wingdi.h</i>.

### -field dmDitherType

Specifies one of the DMDITHER-prefixed constants defined in <i>wingdi.h</i>.

### -field dmReserved1

Is reserved for system use and should be ignored by the driver.

### -field dmReserved2

Is reserved for system use and should be ignored by the driver.

### -field dmPanningWidth

Is reserved for system use and should be ignored by the driver.

### -field dmPanningHeight

Is reserved for system use and should be ignored by the driver.


##### - dmDisplayFlags.DM_GRAYSCALE

Specifies that the display is not a color device. If this flag is not set, color is assumed.


##### - dmDisplayFlags.DM_INTERLACED

Specifies that the display mode is interlaced. If the flag is not set, noninterlaced is assumed.

## -remarks

The <a href="/windows-hardware/drivers/display/the-devmodew-structure">DEVMODEW structure</a> is the Unicode version of the <a href="/previous-versions//ms535771(v=vs.85)">DEVMODE </a> structure (described in the Microsoft Windows SDK documentation). While applications can use either the ANSI or Unicode version of the structure, drivers are required to use the Unicode version.

For printer drivers, the DEVMODEW structure is used for specifying printer characteristics required by a print document. It is also used for specifying a printer's default characteristics.

Immediately following a DEVMODEW structure's defined members (often referred to as its public members), there can be a set of driver-defined members (often referred to as private DEVMODEW members). The driver supplies the size, in bytes, of this private area in <b>dmDriverExtra</b>. Driver-defined private members are for exclusive use by the driver. The starting address for the private members can be referenced using the <b>dmSize</b> member as follows:


```
PVOID pvDriverData = (PVOID) (((BYTE *) pdm) + (pdm->dmSize));
```


A driver can rely on the spooler to pass a DEVMODEW buffer that is no smaller than (<b>dmSize</b> + <b>dmDriverExtra</b>) bytes. As a result, the driver can safely read that number of bytes starting from the beginning of the buffer without causing an access violation, and without needing to probe memory.

Prior to playing EMF, GDI calls the spooler to validate the contents of the public portion of the DEVMODEW buffer. If the DEVMODEW buffer does not pass the validation tests performed in the spooler, GDI does not pass the buffer on to the printer driver.

<div class="alert"><b>Warning</b>    Windows only confirms that the public portion of DEVMODEW is valid. However, corrupted data in the private portion of the structure can cause driver code to crash in the application or in the spooler process. Consequently, before each use of DEVMODEW data the driver should verify that the private portion of DEVMODEW is well-formed.</div>
<div> </div>
In Windows 2000, a new <b>union</b> member was added to the DEVMODEW structure. This <b>union</b> member contains an existing DEVMODEW structure member, <b>dmDisplayFlags</b>, together with a new member, <b>dmNup</b>. This member is described in the preceding Members section.

In Windows XP, a new <b>struct</b> member was added. This <b>struct</b> member contains an existing DEVMODEW structure member, <b>dmPosition</b>, together with two new members, <b>dmDisplayOrientation</b> and <b>dmDisplayFixedOutput</b>. These members are described in the preceding Members section. 

Also for Windows XP, several members of the DEVMODEW structure were moved to different locations in this structure. The <b>dmScale</b>, <b>dmCopies</b>, <b>dmDefaultSource</b>, and <b>dmPrintQuality</b> members were appended to the <b>struct</b> member containing the <b>dmOrientation</b>, <b>dmPaperSize</b>, <b>dmPaperLength</b>, and <b>dmPaperWidth</b> members.





> [!NOTE]
> The wingdi.h header defines DEVMODE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/ddi/content/winddiui/ns-winddiui-_documentpropertyheader">DOCUMENTPROPERTYHEADER</a>



<a href="/windows-hardware/drivers/ddi/content/winddiui/nf-winddiui-drvconvertdevmode">DrvConvertDevMode</a>



<a href="/windows-hardware/drivers/ddi/content/winddiui/nf-winddiui-drvdevicecapabilities">DrvDeviceCapabilities</a>



<a href="/windows/win32/api/winddi/nf-winddi-drvgetmodes">DrvGetModes</a>
