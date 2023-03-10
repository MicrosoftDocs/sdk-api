---
UID: NS:tapi.phonecaps_tag
title: PHONECAPS (tapi.h)
description: The PHONECAPS structure describes the capabilities of a phone device. The phoneGetDevCaps and TSPI_phoneGetDevCaps functions return this structure.
helpviewer_keywords: ["*LPPHONECAPS","LPPHONECAPS","LPPHONECAPS structure pointer [TAPI 2.2]","PHONECAPS","PHONECAPS structure [TAPI 2.2]","_tapi2_phonecaps_str","tapi/LPPHONECAPS","tapi/PHONECAPS","tapi2.phonecaps_str"]
old-location: tapi2\phonecaps_str.htm
tech.root: tapi3
ms.assetid: 9549e30c-9425-4fb1-8ce5-f180a32f8e1f
ms.date: 12/05/2018
ms.keywords: '*LPPHONECAPS, LPPHONECAPS, LPPHONECAPS structure pointer [TAPI 2.2], PHONECAPS, PHONECAPS structure [TAPI 2.2], _tapi2_phonecaps_str, tapi/LPPHONECAPS, tapi/PHONECAPS, tapi2.phonecaps_str'
req.header: tapi.h
req.include-header: 
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
req.typenames: PHONECAPS, *LPPHONECAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phonecaps_tag
 - tapi/phonecaps_tag
 - LPPHONECAPS
 - tapi/LPPHONECAPS
 - PHONECAPS
 - tapi/PHONECAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - PHONECAPS
---

# PHONECAPS structure


## -description

The 
<b>PHONECAPS</b> structure describes the capabilities of a phone device. The 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a> functions return this structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwProviderInfoSize

Size of the provider-specific information, in bytes. If the provider-specific information is a pointer to a string, the size must include the <b>null</b> terminator.

### -field dwProviderInfoOffset

Offset from the beginning of the structure to the variably sized field containing service provider-specific information. 




This member provides information about the provider hardware and/or software, such as the vendor name and version numbers of hardware and software. This information can be useful when a user needs to call customer service with problems regarding the provider. The size of the field is specified by <b>dwProviderInfoSize</b>.

### -field dwPhoneInfoSize

Size of the phone-specific information, in bytes. If the phone-specific information is a pointer to a string, the size must include the <b>null</b> terminator.

### -field dwPhoneInfoOffset

Offset from the beginning of the structure to the variably sized device field containing phone-specific information. 




This member provides information about the attached phone device, such as the phone device manufacturer, the model name, the software version, and so on. This information can be useful when a user needs to call customer service with problems regarding the phone. The size of the field is specified by <b>dwPhoneInfoSize</b>.

### -field dwPermanentPhoneID

Permanent identifier by which the phone device is known in the system's configuration.

### -field dwPhoneNameSize

Size of the configurable name for the phone, including the <b>null</b> terminator, in bytes.

### -field dwPhoneNameOffset

Offset from the beginning of the structure to the variably sized device field containing a user configurable name for this phone device. This name can be configured by the user when configuring the phone device's service provider and is provided for the user's convenience. The size of the field is specified by <b>dwPhoneNameSize</b>.

### -field dwStringFormat

String format to be used with this phone device. This member uses one of the 
<a href="/windows/desktop/Tapi/stringformat--constants">STRINGFORMAT_ Constants</a>.

### -field dwPhoneStates

State changes for this phone device for which the application can be notified in a 
<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a> message. This member one or more of the 
<a href="/windows/desktop/Tapi/phonestate--constants">PHONESTATE_ Constants</a>.

### -field dwHookSwitchDevs

Phone's hookswitch devices. This member uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

### -field dwHandsetHookSwitchModes

Hookswitch mode of the handset. The member is only meaningful if the hookswitch device is listed in <b>dwHookSwitchDevs</b>. It uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_ Constants</a>.

### -field dwSpeakerHookSwitchModes

Hookswitch mode of the speaker. The member is only meaningful if the hookswitch device is listed in <b>dwHookSwitchDevs</b>. It uses one of the PHONEHOOKSWITCHMODE_ Constants.

### -field dwHeadsetHookSwitchModes

Hookswitch mode of the headset. The member is only meaningful if the hookswitch device is listed in <b>dwHookSwitchDevs</b>. It uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_ Constants</a>.

### -field dwVolumeFlags

Volume-setting capabilities of the phone device's speaker components. If the bit in position PHONEHOOKSWITCHDEV_ is <b>TRUE</b>, the volume of the corresponding hookswitch device's speaker component can be adjusted with 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesetvolume">phoneSetVolume</a>.

### -field dwGainFlags

Gain-setting capabilities of the phone device's microphone components. If the bit position PHONEHOOKSWITCHDEV_ is <b>TRUE</b>, the volume of the corresponding hookswitch device's microphone component can be adjusted with 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesetgain">phoneSetGain</a>.

### -field dwDisplayNumRows

Display capabilities of the phone device by describing the number of rows in the phone display. The <b>dwDisplayNumRows</b> and <b>dwDisplayNumColumns</b> members are both zero for a phone device without a display.

### -field dwDisplayNumColumns

Display capabilities of the phone device by describing the number of columns in the phone display. The <b>dwDisplayNumRows</b> and <b>dwDisplayNumColumns</b> members are both zero for a phone device without a display.

### -field dwNumRingModes

Ring capabilities of the phone device. The phone is able to ring with <b>dwNumRingModes</b> different ring patterns, identified as 1, 2, through <b>dwNumRingModes</b> minus one. If the value of this member is 0, applications have no control over the ring mode of the phone. If the value of this member is greater than 0, it indicates the number of ring modes in addition to silence that are supported by the service provider. A value of 0 in the <i>lpdwRingMode</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetring">phoneGetRing</a> or the <i>dwRingMode</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesetring">phoneSetRing</a> indicates silence (the phone is not ringing or should not be rung), and <i>dwRingMode</i> values of 1 to <b>dwNumRingModes</b> are valid ring modes for the phone device.

### -field dwNumButtonLamps

Number of button/lamps on the phone device that are detectable in TAPI. Button/lamps are identified by their identifier. Valid button/lamp identifiers range from zero to <b>dwNumButtonLamps</b> minus one. The keypad buttons '0', through '9', '*', and '#' are assigned the identifiers 0 through 12.

### -field dwButtonModesSize

Size of the button modes array, in bytes.

### -field dwButtonModesOffset

Offset from the beginning of this structure to the variably sized field containing the button modes of the phone's buttons. The array is indexed by button/lamp identifier. This array uses the 
<a href="/windows/desktop/Tapi/phonebuttonmode--constants">PHONEBUTTONMODE_ Constants</a>. The size of the array is specified by <b>dwButtonModesSize</b>.

### -field dwButtonFunctionsSize

Size of the button functions field, in bytes.

### -field dwButtonFunctionsOffset

Offset from the beginning of this structure to the variably sized field containing the button functions of the phone's buttons. The array is indexed by button/lamp identifier. This array uses the 
<a href="/windows/desktop/Tapi/phonebuttonfunction--constants">PHONEBUTTONFUNCTION_ Constants</a>. The size of the array is specified by <b>dwButtonFunctionsSize</b>.

### -field dwLampModesSize

Size of the lamp modes array, in bytes.

### -field dwLampModesOffset

Offset from the beginning of this structure to the variably sized field containing the lamp modes of the phone's lamps. The array is indexed by button/lamp identifier. This array uses the 
<a href="/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ Constants</a>. The size of the array is specified by <b>dwLampModesSize</b>.

### -field dwNumSetData

Number of different download areas in the phone device. The different areas are referred to using the data IDs 0, 1, , <b>dwNumSetData</b> minus one. If this member is zero, the phone does not support the download capability.

### -field dwSetDataSize

Size of the data size array, in bytes.

### -field dwSetDataOffset

Offset from the beginning of this structure to the variably sized field containing the sizes (in bytes) of the phone's download data areas. This is an array with <b>DWORD</b>-sized elements indexed by data identifier. The size of the array is specified by <b>dwSetDataSize</b>.

### -field dwNumGetData

Number of different upload areas in the phone device. The different areas are referred to using the data IDs 0, 1, , <b>dwNumGetData</b> minus one. If this field is zero, the phone does not support the upload capability.

### -field dwGetDataSize

Size of the data size array, in bytes.

### -field dwGetDataOffset

Offset from the beginning of this structure to the variably sized field containing the sizes (in bytes) of the phone's upload data areas. This is an array with <b>DWORD</b>-sized elements indexed by data identifier. The size of the array is specified by <b>dwGetDataSize</b>.

### -field dwDevSpecificSize

Size of the device-specific field, in bytes. If the device specific information is a pointer to a string, the size must include the <b>null</b> terminator.

### -field dwDevSpecificOffset

Offset from the beginning of this structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.

### -field dwDeviceClassesSize

Size of the supported device class identifiers, in bytes.

### -field dwDeviceClassesOffset

Offset from the beginning of this structure to a string consisting of the device class identifiers supported on this device for use with 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a>. The identifiers are separated by <b>NULL</b>s, and the last identifier in the list is followed by two <b>NULL</b>s. The size of the field is specified by <b>dwDeviceClassesSize</b>.

### -field dwPhoneFeatures

Flags that indicate which Telephony API functions can be invoked on the phone. A zero indicates the corresponding feature is not implemented and can never be invoked by the application on the phone; a one indicates the feature may be invoked depending on the device state and other factors. This member uses 
<a href="/windows/desktop/Tapi/phonefeature--constants">PHONEFEATURE_ Constants</a>.

### -field dwSettableHandsetHookSwitchModes

<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_</a> values that can be set on the handset using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesethookswitch">phoneSetHookSwitch</a>.

### -field dwSettableSpeakerHookSwitchModes

PHONEHOOKSWITCHMODE_ values that can be set on the speakerphone using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesethookswitch">phoneSetHookSwitch</a>.

### -field dwSettableHeadsetHookSwitchModes

PHONEHOOKSWITCHMODE_ values that can be set on the headset using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesethookswitch">phoneSetHookSwitch</a>.

### -field dwMonitoredHandsetHookSwitchModes

PHONEHOOKSWITCHMODE_ values that can be detected and reported for the handset in a 
<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a> message and by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegethookswitch">phoneGetHookSwitch</a>.

### -field dwMonitoredSpeakerHookSwitchModes

PHONEHOOKSWITCHMODE_ values that can be detected and reported for the speakerphone in a PHONE_STATE message and by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesethookswitch">phoneSetHookSwitch</a>.

### -field dwMonitoredHeadsetHookSwitchModes

<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_</a> values that can be detected and reported for the headset in a PHONE_STATE message and by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesethookswitch">phoneSetHookSwitch</a>.

### -field PermanentPhoneGuid

The GUID permanently associated with this phone.

## -remarks

Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

The members <b>dwDeviceClassesSize</b> through <b>dwMonitoredHeadsetHookSwitchModes</b> are available only to applications that open the phone device with an API version of 2.0 or later.

## -see-also

<a href="/windows/desktop/Tapi/phone-button">PHONE_BUTTON</a>



<a href="/windows/desktop/Tapi/phone-close">PHONE_CLOSE</a>



<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegethookswitch">phoneGetHookSwitch</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetring">phoneGetRing</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonesetgain">phoneSetGain</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonesethookswitch">phoneSetHookSwitch</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonesetring">phoneSetRing</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonesetvolume">phoneSetVolume</a>