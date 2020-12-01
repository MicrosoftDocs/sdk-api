---
UID: NF:mmeapi.mixerMessage
title: mixerMessage function (mmeapi.h)
description: The mixerMessage function sends a custom mixer driver message directly to a mixer driver.
helpviewer_keywords: ["_win32_mixerMessage","mixerMessage","mixerMessage function [Windows Multimedia]","mmeapi/mixerMessage","multimedia.mixermessage"]
old-location: multimedia\mixermessage.htm
tech.root: Multimedia
ms.assetid: 021669bb-144b-4107-955c-c4cc9cd53c00
ms.date: 12/05/2018
ms.keywords: _win32_mixerMessage, mixerMessage, mixerMessage function [Windows Multimedia], mmeapi/mixerMessage, multimedia.mixermessage
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mixerMessage
 - mmeapi/mixerMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - mixerMessage
---

# mixerMessage function


## -description

The <b>mixerMessage</b> function sends a custom mixer driver message directly to a mixer driver.

## -parameters

### -param hmx

Identifier of the mixer that receives the message. You must cast the device ID to the <b>HMIXER</b> handle type. If you supply a handle instead of a device ID, the function fails and returns the MMSYSERR_NOSUPPORT error code.

### -param uMsg

Custom mixer driver message to send to the mixer driver. This message must be above or equal to the MXDM_USER constant.

### -param dwParam1

Parameter associated with the message being sent.

### -param dwParam2

Parameter associated with the message being sent.

## -returns

Returns a value that is specific to the custom mixer driver message. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The <i>uMsg</i> parameter specified in the MXDM_USER message is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOSUPPORT</b></dt>
</dl>
</td>
<td width="60%">
The <i>deviceID</i> parameter must be a valid device ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The mixer device did not process the message.

</td>
</tr>
</table>

## -remarks

User-defined messages must be sent only to a mixer driver that supports the messages. The application should verify that the mixer driver is the driver that supports the message by retrieving the mixer capabilities and checking the <b>wMid</b>, <b>wPid</b>, <b>vDriverVersion</b>, and <b>szPname</b> members of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a> structure.

The <code>DRV_QUERYDEVICEINTERFACE</code> message queries for the device-interface name of a <b>waveIn</b>, <b>waveOut</b>, <b>midiIn</b>, <b>midiOut</b>, or <b>mixer</b> device.

For <code>DRV_QUERYDEVICEINTERFACE</code>, <i>dwParam1</i> is a pointer to a caller-allocated buffer into which the function writes a null-terminated Unicode string containing the device-interface name. If the device has no device interface, the string length is zero.

For <code>DRV_QUERYDEVICEINTERFACE</code>, <i>dwParam2</i> specifies the buffer size in bytes. This is an input parameter to the function. The caller should specify a size that is greater than or equal to the buffer size retrieved by the <a href="/previous-versions/windows/hardware/drivers/ff536364(v=vs.85)">DRV_QUERYDEVICEINTERFACESIZE</a> message.

The DRV_QUERYDEVICEINTERFACE message is supported in Windows Me, and Windows 2000 and later. This message is valid only for the <a href="/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <a href="/previous-versions/dd743865(v=vs.85)">waveOutMessage</a>, <a href="/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, and <b>mixerMessage</b> functions. The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

The following two message constants are used together for the purpose of obtaining device interface names:

<ul>
<li>
DRV_QUERYDEVICEINTERFACESIZE

</li>
<li>
DRV_QUERYDEVICEINTERFACE

</li>
</ul>
The first message obtains the size in bytes of the buffer needed to hold the string containing the device interface name. The second message retrieves the name string in a buffer of the required size.

For more information, see <a href="/windows-hardware/drivers/audio/obtaining-a-device-interface-name">Obtaining a Device Interface Name</a>.

The <code>DRV_QUERYDEVICEINTERFACESIZE</code> message queries for the size of the buffer required to hold the device-interface name.

For <code>DRV_QUERYDEVICEINTERFACESIZE</code>, <i>dwParam1</i> is a pointer to buffer size. This parameter points to a ULONG variable into which the function writes the required buffer size in bytes. The size includes storage space for the name string's terminating null. The size is zero if the device ID identifies a device that has no device interface.

For <code>DRV_QUERYDEVICEINTERFACESIZE</code>, <i>dwParam2</i> is unused. Set this parameter to zero.

This message is valid only for the <a href="/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <a href="/previous-versions/dd743865(v=vs.85)">waveOutMessage</a>, <a href="/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, and <b>mixerMessage</b> functions. The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

The buffer size retrieved by this message is expressed as a byte count. It specifies the size of the buffer needed to hold the null-terminated Unicode string that contains the device-interface name. The caller allocates a buffer of the specified size and uses the <a href="/previous-versions/windows/hardware/drivers/ff536363(v=vs.85)">DRV_QUERYDEVICEINTERFACE</a> message to retrieve the device-interface name string.

For more information, see <a href="/windows-hardware/drivers/audio/obtaining-a-device-interface-name">Obtaining a Device Interface Name</a>.

The <code>DRV_QUERYDEVNODE</code> message queries for the <a href="/windows-hardware/drivers/">devnode</a> number assigned to the device by the Plug and Play manager.

For <code>DRV_QUERYDEVNODE</code>, <i>dwParam1</i> is a pointer to a caller-allocated DWORD variable into which the function writes the devnode number. If no devnode is assigned to the device, the function sets this variable to zero.

For <code>DRV_QUERYDEVNODE</code>, <i>dwParam2</i> is unused. Set this parameter to zero.

In Windows 2000 and later, the message always returns MMSYSERR_NOTSUPPORTED. This message is valid only for the <a href="/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <a href="/previous-versions/dd743865(v=vs.85)">waveOutMessage</a>, <a href="/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, and <b>mixerMessage</b> functions.  The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

The <code>DRV_QUERYMAPPABLE</code> message queries for whether the specified device can be used by a mapper.

For <code>DRV_QUERYMAPPABLE</code>, <i>dwParam1</i> is unused. Set this parameter to zero.

For <code>DRV_QUERYMAPPABLE</code>, <i>dwParam2</i> is unused. Set this parameter to zero.

This message is valid only for the <a href="/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <a href="/previous-versions/dd743865(v=vs.85)">waveOutMessage</a>, <a href="/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, <b>mixerMessage</b> and <a href="/previous-versions/dd756716(v=vs.85)">auxOutMessage</a> functions. The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

When an application program opens a mapper instead of a specific audio device, the system inserts a mapper between the application and the available devices. The mapper selects an appropriate device by mapping the application's requirements to one of the available devices. For more information about mappers, see the Microsoft Windows SDK documentation.

The <code>DRVM_MAPPER_CONSOLEVOICECOM_GET</code> message retrieves the device ID of the preferred voice-communications device.

For <code>DRVM_MAPPER_CONSOLEVOICECOM_GET</code>, <i>dwParam1</i> is a pointer to device ID. This parameter points to a DWORD variable into which the function writes the device ID of the current preferred voice-communications device. The function writes the value (-1) if no device is available that qualifies as a preferred voice-communications device.

For <code>DRVM_MAPPER_CONSOLEVOICECOM_GET</code>, <i>dwParam2</i> is a pointer to status flags. This parameter points to a DWORD variable into which the function writes the device-status flags. Only one flag bit is currently defined: DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY. 

This message is valid only for the <a href="/previous-versions/dd743846(v=vs.85)">waveInMessage</a> and <a href="/previous-versions/dd743865(v=vs.85)">waveOutMessage</a> functions. When a caller calls these two functions with the DRVM_MAPPER_CONSOLEVOICECOM_GET message, the caller must specify the device ID as WAVE_MAPPER, and then cast this value to the appropriate handle type. For the <b>waveInMessage</b>, <b>waveOutMessage</b>, <a href="/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, or <b>mixerMessage</b> functions, the caller must cast the device ID to a handle of type HWAVEIN, HWAVEOUT, HMIDIIN, HMIDIOUT, or HMIXER, respectively. Note that if the caller supplies a valid handle instead of a device ID for this parameter, the function fails and returns error code MMSYSERR_NOSUPPORT.

The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

This message provides a way to determine which device is preferred specifically for voice communications, in contrast to the <a href="/previous-versions/windows/hardware/drivers/ff536362(v=vs.85)">DRVM_MAPPER_PREFERRED_GET</a> message, which determines which device is preferred for all other audio functions.

For example, the preferred <b>waveOut</b> device for voice communications might be the earpiece in a headset, but the preferred <b>waveOut</b> device for all other audio functions might be a set of stereo speakers.

When the DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY flag bit is set in the DWORD location pointed to by <i>dwParam2</i>, the <b>waveIn</b> and <b>waveOut</b> APIs use only the current preferred voice-communications device and do not search for other available devices if the preferred device is unavailable. The flag that is output by either the <b>waveInMessage</b> or <b>waveOutMessage</b> call applies to the preferred voice-communications device for both the <b>waveIn</b> and <b>waveOut</b> APIs, regardless of whether the call is made to <b>waveInMessage</b> or <b>waveOutMessage</b>. For more information, see <a href="/windows-hardware/drivers/audio/preferred-voice-communications-device-id">Preferred Voice-Communications Device ID</a>.

The <code>DRVM_MAPPER_PREFERRED_GET</code> message retrieves the device ID of the preferred audio device.

For <code>DRVM_MAPPER_PREFERRED_GET</code>, <i>dwParam1</i> is a pointer to device ID. This parameter points to a DWORD variable into which the function writes the device ID of the current preferred device. The function writes the value (-1) if no device is available that qualifies as a preferred device.

For <code>DRVM_MAPPER_PREFERRED_GET</code>, <i>dwParam2</i> is a pointer to status flags. This parameter points to a DWORD variable into which the function writes the device-status flags. Only one flag bit is currently defined (for <b>waveInMessage</b> and <b>waveOutMessage</b> calls only): DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY. 

This message is valid only for the <a href="/previous-versions/dd743846(v=vs.85)">waveInMessage</a>,  <a href="/previous-versions/dd743865(v=vs.85)">waveOutMessage</a> and  <a href="/previous-versions/dd798475(v=vs.85)">midiOutMessage</a> functions. When the caller calls these functions with the DRVM_MAPPER_PREFERRED_GET message, the caller must first specify the device ID as WAVE_MAPPER (for <b>waveInMessage</b> or <b>waveOutMessage</b>) or MIDI_MAPPER (for <b>midiOutMessage</b>), and then cast this value to the appropriate handle type. For the <b>waveInMessage</b>, <b>waveOutMessage</b>, or <b>midiOutMessage</b> functions, the caller must cast the device ID to a handle type HWAVEIN, HWAVEOUT or HMIDIOUT, respectively. Note that if the caller supplies a valid handle instead of a device ID for this parameter, the function fails and returns error code MMSYSERR_NOSUPPORT.

The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

This message provides a way to determine which device is preferred for audio functions in general, in contrast to the <a href="/previous-versions/windows/hardware/drivers/ff536361(v=vs.85)">DRVM_MAPPER_CONSOLEVOICECOM_GET</a> message, which determines which device is preferred specifically for voice communications.

When the DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY flag bit is set in the DWORD location pointed to by <i>dwParam2</i>, the <b>waveIn</b> and <b>waveOut</b> APIs use only the current preferred device and do not search for other available devices if the preferred device is unavailable. Note that the <b>midiOutMessage</b> function does not output this flag--the <b>midiOut</b> API always uses only the preferred device. The flag that is output by either the <b>waveInMessage</b> or <b>waveOutMessage</b> call applies to the preferred device for both the <b>waveIn</b> and <b>waveOut</b> APIs, regardless of whether the call is made to <b>waveInMessage</b> or <b>waveOutMessage</b>.

The <i>xxx</i>Message functions accept this value in place of a valid device handle in order to allow an application to determine the default device ID without first having to open a device. For more information, see <a href="/windows-hardware/drivers/audio/accessing-the-preferred-device-id">Accessing the Preferred Device ID</a>.

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>