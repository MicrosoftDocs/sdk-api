---
UID: NS:msacm.tACMDRIVERDETAILS
title: ACMDRIVERDETAILS (msacm.h)
description: The ACMDRIVERDETAILS structure describes the features of an ACM driver.
helpviewer_keywords: ["*LPACMDRIVERDETAILS","*PACMDRIVERDETAILS","ACMDRIVERDETAILS","ACMDRIVERDETAILS structure [Windows Multimedia]","ACMDRIVERDETAILS_SUPPORTF_ASYNC","ACMDRIVERDETAILS_SUPPORTF_CODEC","ACMDRIVERDETAILS_SUPPORTF_CONVERTER","ACMDRIVERDETAILS_SUPPORTF_DISABLED","ACMDRIVERDETAILS_SUPPORTF_FILTER","ACMDRIVERDETAILS_SUPPORTF_HARDWARE","ACMDRIVERDETAILS_SUPPORTF_LOCAL","msacm/ACMDRIVERDETAILS","multimedia.acmdriverdetails_COLLISION566","multimedia.acmdriverdetails_struct"]
old-location: multimedia\acmdriverdetails_struct.htm
tech.root: Multimedia
ms.assetid: b45b26e2-a9c0-4d01-9989-a071d9c73993
ms.date: 12/05/2018
ms.keywords: '*LPACMDRIVERDETAILS, *PACMDRIVERDETAILS, ACMDRIVERDETAILS, ACMDRIVERDETAILS structure [Windows Multimedia], ACMDRIVERDETAILS_SUPPORTF_ASYNC, ACMDRIVERDETAILS_SUPPORTF_CODEC, ACMDRIVERDETAILS_SUPPORTF_CONVERTER, ACMDRIVERDETAILS_SUPPORTF_DISABLED, ACMDRIVERDETAILS_SUPPORTF_FILTER, ACMDRIVERDETAILS_SUPPORTF_HARDWARE, ACMDRIVERDETAILS_SUPPORTF_LOCAL, msacm/ACMDRIVERDETAILS, multimedia.acmdriverdetails_COLLISION566, multimedia.acmdriverdetails_struct'
req.header: msacm.h
req.include-header: 
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
req.typenames: ACMDRIVERDETAILS, *PACMDRIVERDETAILS, *LPACMDRIVERDETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMDRIVERDETAILS
 - msacm/tACMDRIVERDETAILS
 - PACMDRIVERDETAILS
 - msacm/PACMDRIVERDETAILS
 - ACMDRIVERDETAILS
 - msacm/ACMDRIVERDETAILS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msacm.h
api_name:
 - ACMDRIVERDETAILS
---

# ACMDRIVERDETAILS structure


## -description

The <b>ACMDRIVERDETAILS</b> structure describes the features of an ACM driver.

## -struct-fields

### -field cbStruct

Size, in bytes, of the valid information contained in the <b>ACMDRIVERDETAILS</b> structure. An application should initialize this member to the size, in bytes, of the desired information. The size specified in this member must be large enough to contain the <b>cbStruct</b> member of the <b>ACMDRIVERDETAILS</b> structure. When the <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverdetails">acmDriverDetails</a> function returns, this member contains the actual size of the information returned. The returned information will never exceed the requested size.

### -field fccType

Type of the driver. For ACM drivers, set this member to ACMDRIVERDETAILS_FCCTYPE_AUDIOCODEC.

### -field fccComp

Subtype of the driver. This member is currently set to ACMDRIVERDETAILS_FCCCOMP_UNDEFINED (zero).

### -field wMid

Manufacturer identifier. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

Product identifier. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field vdwACM

Version of the ACM for which this driver was compiled. The version number is a hexadecimal number in the format 0xAABBCCCC, where AA is the major version number, BB is the minor version number, and CCCC is the build number. The version parts (major, minor, and build) should be displayed as decimal numbers.

### -field vdwDriver

Version of the driver. The version number is a hexadecimal number in the format 0xAABBCCCC, where AA is the major version number, BB is the minor version number, and CCCC is the build number. The version parts (major, minor, and build) should be displayed as decimal numbers.

### -field fdwSupport

Support flags for the driver. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_ASYNC"></a><a id="acmdriverdetails_supportf_async"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports asynchronous conversions.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CODEC"></a><a id="acmdriverdetails_supportf_codec"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CODEC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different format tags. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CONVERTER"></a><a id="acmdriverdetails_supportf_converter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different formats of the same format tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_DISABLED"></a><a id="acmdriverdetails_supportf_disabled"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Driver has been disabled. This flag is set by the ACM for a driver when it has been disabled for any of a number of reasons. Disabled drivers cannot be opened and can be used only under very limited circumstances.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_FILTER"></a><a id="acmdriverdetails_supportf_filter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_HARDWARE"></a><a id="acmdriverdetails_supportf_hardware"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
Driver supports hardware input, output, or both through a waveform-audio device. An application should use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_LOCAL"></a><a id="acmdriverdetails_supportf_local"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The driver has been installed locally with respect to the current task.

</td>
</tr>
</table>

### -field cFormatTags

Number of unique format tags supported by this driver.

### -field cFilterTags

Number of unique filter tags supported by this driver.

### -field hicon

Handle to a custom icon for this driver. An application can use this icon for referencing the driver visually. This member can be <b>NULL</b>.

### -field szShortName

Null-terminated string that describes the name of the driver. This string is intended to be displayed in small spaces.

### -field szLongName

Null-terminated string that describes the full name of the driver. This string is intended to be displayed in large (descriptive) spaces.

### -field szCopyright

Null-terminated string that provides copyright information for the driver.

### -field szLicensing

Null-terminated string that provides special licensing information for the driver.

### -field szFeatures

Null-terminated string that provides special feature information for the driver.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmdriverdetails">acmDriverDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a>