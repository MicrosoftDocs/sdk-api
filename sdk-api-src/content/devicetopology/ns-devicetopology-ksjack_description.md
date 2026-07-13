---
UID: NS:devicetopology.__MIDL___MIDL_itf_devicetopology_0000_0000_0009
title: KSJACK_DESCRIPTION (devicetopology.h)
description: The KSJACK_DESCRIPTION structure describes an audio jack.
old-location: coreaudio\ksjack_description.htm
tech.root: CoreAudio
ms.assetid: 4ee9fedf-4241-4678-b621-549a06e8949a
ms.date: 12/05/2018
ms.keywords: '*PKSJACK_DESCRIPTION, KSJACK_DESCRIPTION, KSJACK_DESCRIPTION structure [Core Audio], PKSJACK_DESCRIPTION, PKSJACK_DESCRIPTION structure pointer [Core Audio], coreaudio.ksjack_description, devicetopology/KSJACK_DESCRIPTION, devicetopology/PKSJACK_DESCRIPTION'
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: KSJACK_DESCRIPTION, *PKSJACK_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_devicetopology_0000_0000_0009
 - devicetopology/__MIDL___MIDL_itf_devicetopology_0000_0000_0009
 - PKSJACK_DESCRIPTION
 - devicetopology/PKSJACK_DESCRIPTION
 - KSJACK_DESCRIPTION
 - devicetopology/KSJACK_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - KSJACK_DESCRIPTION
---

# KSJACK_DESCRIPTION structure


## -description

The <b>KSJACK_DESCRIPTION</b> structure describes an audio jack.

## -struct-fields

### -field ChannelMapping

Specifies the mapping of the two audio channels in a stereo jack to speaker positions. 

In Windows Vista, the value of this member is one of the <b>EChannelMapping</b> enumeration values shown in the following table.<table>
<tr>
<th>Value</th>
<th>First channel</th>
<th>Second channel</th>
</tr>
<tr>
<td>ePcxChanMap_FL_FR</td>
<td>Front-left speaker</td>
<td>Front-right speaker</td>
</tr>
<tr>
<td>ePcxChanMap_FC_LFE</td>
<td>Front-center speaker</td>
<td>Low-frequency-effects speaker (subwoofer)</td>
</tr>
<tr>
<td>ePcxChanMap_BL_BR</td>
<td>Back-left speaker</td>
<td>Back-right speakers</td>
</tr>
<tr>
<td>ePcxChanMap_FLC_FRC</td>
<td>Front-left-center speaker</td>
<td>Front-right-center speaker</td>
</tr>
<tr>
<td>ePcxChanMap_SL_SR</td>
<td>Side-left speaker</td>
<td>Side-right speaker</td>
</tr>
<tr>
<td>ePcxChanMap_Unknown</td>
<td>Unknown</td>
<td>Unknown</td>
</tr>
</table>
 </p>For a physical connector with one, three, or more channels, the value of this member is ePcxChanMap_Unknown.

In Windows 7, the <b>EChannelMapping</b> enumeration has been deprecated. The datatype of this member is a <b>DWORD</b>.  This member stores either 0 or the bitwise-OR combination of one or more of the following values that are defined in Ksmedia.h.



``` syntax
#define SPEAKER_FRONT_LEFT              0x1
#define SPEAKER_FRONT_RIGHT             0x2
#define SPEAKER_FRONT_CENTER            0x4
#define SPEAKER_LOW_FREQUENCY           0x8
#define SPEAKER_BACK_LEFT               0x10
#define SPEAKER_BACK_RIGHT              0x20
#define SPEAKER_FRONT_LEFT_OF_CENTER    0x40
#define SPEAKER_FRONT_RIGHT_OF_CENTER   0x80
#define SPEAKER_BACK_CENTER             0x100
#define SPEAKER_SIDE_LEFT               0x200
#define SPEAKER_SIDE_RIGHT              0x400
#define SPEAKER_TOP_CENTER              0x800
#define SPEAKER_TOP_FRONT_LEFT          0x1000
#define SPEAKER_TOP_FRONT_CENTER        0x2000
#define SPEAKER_TOP_FRONT_RIGHT         0x4000
#define SPEAKER_TOP_BACK_LEFT           0x8000
#define SPEAKER_TOP_BACK_CENTER         0x10000
#define SPEAKER_TOP_BACK_RIGHT          0x20000

```


### -field Color

The jack color. The color is expressed as a 32-bit RGB value that is formed by concatenating the 8-bit blue, green, and red color components. The blue component occupies the 8 least-significant bits (bits 0-7), the green component occupies bits 8-15, and the red component occupies bits 16-23. The 8 most-significant bits are zeros. If the jack color is unknown or the physical connector has no identifiable color, the value of this member is 0x00000000, which is black.

### -field ConnectionType

The connection type. The value of this member is one of the <b>EPcxConnectionType</b> enumeration values shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Connector type</th>
</tr>
<tr>
<td>eConnTypeUnknown</td>
<td>Unknown</td>
</tr>
<tr>
<td>
eConnTypeEighth (Windows Vista)

 eConnType3Point5mm</p> (Windows 7)
                  </td>
<td>1/8-inch jack</td>
</tr>
<tr>
<td>eConnTypeQuarter</td>
<td>1/4-inch jack</td>
</tr>
<tr>
<td>eConnTypeAtapiInternal</td>
<td>ATAPI internal connector</td>
</tr>
<tr>
<td>eConnTypeRCA</td>
<td>RCA jack</td>
</tr>
<tr>
<td>eConnTypeOptical</td>
<td>Optical connector</td>
</tr>
<tr>
<td>eConnTypeOtherDigital</td>
<td>Generic digital connector</td>
</tr>
<tr>
<td>eConnTypeOtherAnalog</td>
<td>Generic analog connector</td>
</tr>
<tr>
<td>eConnTypeMultichannelAnalogDIN</td>
<td>Multichannel analog DIN connector</td>
</tr>
<tr>
<td>eConnTypeXlrProfessional</td>
<td>XLR connector</td>
</tr>
<tr>
<td>eConnTypeRJ11Modem</td>
<td>RJ11 modem connector</td>
</tr>
<tr>
<td>eConnTypeCombination</td>
<td>Combination of connector types</td>
</tr>
</table>

### -field GeoLocation

The geometric location of the jack. The value of this member is one of the <b>EPcxGeoLocation</b> enumeration values shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Geometric location</th>
</tr>
<tr>
<td>eGeoLocRear</td>
<td>Rear-mounted panel</td>
</tr>
<tr>
<td>eGeoLocFront</td>
<td>Front-mounted panel</td>
</tr>
<tr>
<td>eGeoLocLeft</td>
<td>Left-mounted panel</td>
</tr>
<tr>
<td>eGeoLocRight</td>
<td>Right-mounted panel</td>
</tr>
<tr>
<td>eGeoLocTop</td>
<td>Top-mounted panel</td>
</tr>
<tr>
<td>eGeoLocBottom</td>
<td>Bottom-mounted panel</td>
</tr>
<tr>
<td>
eGeoLocRearOPanel(Windows Vista)

eGeoLocRearPanel(Windows 7)
                  

</td>
<td> Rear slide-open or pull-open panel</td>
</tr>
<tr>
<td>eGeoLocRiser</td>
<td>Riser card</td>
</tr>
<tr>
<td>eGeoLocInsideMobileLid</td>
<td>Inside lid of mobile computer</td>
</tr>
<tr>
<td>eGeoLocDrivebay</td>
<td>Drive bay</td>
</tr>
<tr>
<td>eGeoLocHDMI</td>
<td>HDMI connector</td>
</tr>
<tr>
<td>eGeoLocOutsideMobileLid</td>
<td>Outside lid of mobile computer</td>
</tr>
<tr>
<td>eGeoLocATAPI</td>
<td>ATAPI connector</td>
</tr>
</table>

### -field GenLocation

The general location of the jack. The value of this member is one of the <b>EPcxGenLocation</b> enumeration values shown in the following table.

<table>
<tr>
<th>Value</th>
<th>General location</th>
</tr>
<tr>
<td>eGenLocPrimaryBox</td>
<td>On primary chassis</td>
</tr>
<tr>
<td>eGenLocInternal</td>
<td>Inside primary chassis</td>
</tr>
<tr>
<td>
eGenLocSeperate(Windows Vista)

eGenLocSeparate(Windows 7)
                  

</td>
<td>On separate chassis</td>
</tr>
<tr>
<td>eGenLocOther</td>
<td>Other location</td>
</tr>
</table>

### -field PortConnection

The type of port represented by the jack. The value of this member is one of the <b>EPxcPortConnection</b> enumeration values shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Port connection type</th>
</tr>
<tr>
<td>ePortConnJack</td>
<td>Jack</td>
</tr>
<tr>
<td>ePortConnIntegratedDevice</td>
<td>Slot for an integrated device</td>
</tr>
<tr>
<td>ePortConnBothIntegratedAndJack</td>
<td>Both a jack and a slot for an integrated device</td>
</tr>
<tr>
<td>ePortConnUnknown</td>
<td>Unknown</td>
</tr>
</table>

### -field IsConnected

If the audio adapter supports jack-presence detection on the jack, the value of <b>IsConnected</b> indicates whether an endpoint device is plugged into the jack. If <b>IsConnected</b> is <b>TRUE</b>, a device is plugged in. If it is <b>FALSE</b>, the jack is empty. For devices that do not support jack-presence detection, this member is always <b>TRUE</b>. For more information about jack-presence detection, see <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">Audio Endpoint Devices</a>.

## -remarks

This structure is used by the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription-getjackdescription">IKsJackDescription::GetJackDescription</a> method in the <a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>. It describes an audio jack that is part of a connection between an endpoint device and a hardware device in an audio adapter. When a user needs to plug an endpoint device into a jack or unplug it from a jack, an audio application can use the descriptive information in the structure to help the user to find the jack.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription-getjackdescription">IKsJackDescription::GetJackDescription</a>
