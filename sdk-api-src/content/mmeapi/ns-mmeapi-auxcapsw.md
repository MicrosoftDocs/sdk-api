---
UID: NS:mmeapi.tagAUXCAPSW
title: AUXCAPSW (mmeapi.h)
description: The AUXCAPS structure describes the capabilities of an auxiliary output device.
helpviewer_keywords: ["*LPAUXCAPSW","*NPAUXCAPSW","*PAUXCAPSW","AUXCAPS","AUXCAPS structure [Windows Multimedia]","AUXCAPSA","AUXCAPSW","AUXCAPS_AUXIN","AUXCAPS_CDAUDIO","AUXCAPS_LRVOLUME","AUXCAPS_VOLUME","_win32_AUXCAPS_str","auxcaps_tag","mmeapi/AUXCAPS","multimedia.auxcaps"]
old-location: multimedia\auxcaps.htm
tech.root: Multimedia
ms.assetid: 5b94a468-88b2-40a4-b28d-49f262e62749
ms.date: 12/05/2018
ms.keywords: '*LPAUXCAPSW, *NPAUXCAPSW, *PAUXCAPSW, AUXCAPS, AUXCAPS structure [Windows Multimedia], AUXCAPSA, AUXCAPSW, AUXCAPS_AUXIN, AUXCAPS_CDAUDIO, AUXCAPS_LRVOLUME, AUXCAPS_VOLUME, _win32_AUXCAPS_str, auxcaps_tag, mmeapi/AUXCAPS, multimedia.auxcaps'
f1_keywords:
- mmeapi/AUXCAPS
dev_langs:
- c++
req.header: mmeapi.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mmeapi.h
api_name:
- AUXCAPS
- AUXCAPSW
targetos: Windows
req.typenames: AUXCAPSW, *PAUXCAPSW, *NPAUXCAPSW, *LPAUXCAPSW
req.redist: 
ms.custom: 19H1
---

# AUXCAPSW structure


## -description



The <b>AUXCAPS</b> structure describes the capabilities of an auxiliary output device.




## -struct-fields




### -field wMid

Manufacturer identifier for the device driver for the auxiliary audio device. Manufacturer identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


### -field wPid

Product identifier for the auxiliary audio device. Currently, no product identifiers are defined for auxiliary audio devices.


### -field vDriverVersion

Version number of the device driver for the auxiliary audio device. The high-order byte is the major version number, and the low-order byte is the minor version number.


### -field szPname

Product name in a null-terminated string.


### -field wTechnology

Type of the auxiliary audio output:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AUXCAPS_AUXIN"></a><a id="auxcaps_auxin"></a><dl>
<dt><b>AUXCAPS_AUXIN</b></dt>
</dl>
</td>
<td width="60%">
Audio output from auxiliary input jacks.

</td>
</tr>
<tr>
<td width="40%"><a id="AUXCAPS_CDAUDIO"></a><a id="auxcaps_cdaudio"></a><dl>
<dt><b>AUXCAPS_CDAUDIO</b></dt>
</dl>
</td>
<td width="60%">
Audio output from an internal CD-ROM drive.

</td>
</tr>
</table>
 




### -field dwSupport

Describes optional functionality supported by the auxiliary audio device.

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AUXCAPS_LRVOLUME"></a><a id="auxcaps_lrvolume"></a><dl>
<dt><b>AUXCAPS_LRVOLUME</b></dt>
</dl>
</td>
<td width="60%">
Supports separate left and right volume control.

</td>
</tr>
<tr>
<td width="40%"><a id="AUXCAPS_VOLUME"></a><a id="auxcaps_volume"></a><dl>
<dt><b>AUXCAPS_VOLUME</b></dt>
</dl>
</td>
<td width="60%">
Supports volume control.

</td>
</tr>
</table>
 

If a device supports volume changes, the AUXCAPS_VOLUME flag will be set. If a device supports separate volume changes on the left and right channels, both AUXCAPS_VOLUME and the AUXCAPS_LRVOLUME will be set.

## -remarks

> [!NOTE]
> The mmeapi.h header defines AUXCAPS as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

