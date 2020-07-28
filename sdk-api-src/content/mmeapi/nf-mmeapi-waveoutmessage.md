---
UID: NF:mmeapi.waveOutMessage
title: waveOutMessage function (mmeapi.h)
description: The waveOutMessage function sends messages to the waveform-audio output device drivers.
helpviewer_keywords: ["_win32_waveOutMessage","mmeapi/waveOutMessage","multimedia.waveoutmessage","waveOutMessage","waveOutMessage function [Windows Multimedia]"]
old-location: multimedia\waveoutmessage.htm
tech.root: Multimedia
ms.assetid: b4f06107-781f-4b95-8138-ca0e11a21cf4
ms.date: 12/05/2018
ms.keywords: _win32_waveOutMessage, mmeapi/waveOutMessage, multimedia.waveoutmessage, waveOutMessage, waveOutMessage function [Windows Multimedia]
f1_keywords:
- mmeapi/waveOutMessage
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
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
- waveOutMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# waveOutMessage function


## -description



The <b>waveOutMessage</b> function sends messages to the waveform-audio output device drivers.




## -parameters




### -param hwo

Identifier of the waveform device that receives the message. You must cast the device ID to the <b>HWAVEOUT</b> handle type. If you supply a handle instead of a device ID, the function fails and returns the MMSYSERR_NOSUPPORT error code.


### -param uMsg

Message to send.


### -param dw1

Message parameter.


### -param dw2

Message parameter.


## -returns



Returns the value returned from the driver.




## -remarks



The <code>DRV_QUERYDEVICEINTERFACE</code> message queries for the device-interface name of a <b>waveIn</b>, <b>waveOut</b>, <b>midiIn</b>, <b>midiOut</b>, or <b>mixer</b> device.

For <code>DRV_QUERYDEVICEINTERFACE</code>, <i>dwParam1</i> is a pointer to a caller-allocated buffer into which the function writes a null-terminated Unicode string containing the device-interface name. If the device has no device interface, the string length is zero.

For <code>DRV_QUERYDEVICEINTERFACE</code>, <i>dwParam2</i> specifies the buffer size in bytes. This is an input parameter to the function. The caller should specify a size that is greater than or equal to the buffer size retrieved by the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff536364(v=vs.85)">DRV_QUERYDEVICEINTERFACESIZE</a> message.

The DRV_QUERYDEVICEINTERFACE message is supported in Windows Me, and Windows 2000 and later. This message is valid only for the <a href="https://docs.microsoft.com/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <b>waveOutMessage</b>, <a href="https://docs.microsoft.com/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="https://docs.microsoft.com/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, and <a href="https://docs.microsoft.com/previous-versions/dd757307(v=vs.85)">mixerMessage</a> functions. The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

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

For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/obtaining-a-device-interface-name">Obtaining a Device Interface Name</a>.

The <code>DRV_QUERYDEVICEINTERFACESIZE</code> message queries for the size of the buffer required to hold the device-interface name.

For <code>DRV_QUERYDEVICEINTERFACESIZE</code>, <i>dwParam1</i> is a pointer to buffer size. This parameter points to a ULONG variable into which the function writes the required buffer size in bytes. The size includes storage space for the name string's terminating null. The size is zero if the device ID identifies a device that has no device interface.

For <code>DRV_QUERYDEVICEINTERFACESIZE</code>, <i>dwParam2</i> is unused. Set this parameter to zero.

This message is valid only for the <a href="https://docs.microsoft.com/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <b>waveOutMessage</b>, <a href="https://docs.microsoft.com/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="https://docs.microsoft.com/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, and <a href="https://docs.microsoft.com/previous-versions/dd757307(v=vs.85)">mixerMessage</a> functions. The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

The buffer size retrieved by this message is expressed as a byte count. It specifies the size of the buffer needed to hold the null-terminated Unicode string that contains the device-interface name. The caller allocates a buffer of the specified size and uses the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff536363(v=vs.85)">DRV_QUERYDEVICEINTERFACE</a> message to retrieve the device-interface name string.

For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/obtaining-a-device-interface-name">Obtaining a Device Interface Name</a>.

The <code>DRV_QUERYDEVNODE</code> message queries for the <a href="https://docs.microsoft.com/windows-hardware/drivers/">devnode</a> number assigned to the device by the Plug and Play manager.

For <code>DRV_QUERYDEVNODE</code>, <i>dwParam1</i> is a pointer to a caller-allocated DWORD variable into which the function writes the devnode number. If no devnode is assigned to the device, the function sets this variable to zero.

For <code>DRV_QUERYDEVNODE</code>, <i>dwParam2</i> is unused. Set this parameter to zero.

In Windows 2000 and later, the message always returns MMSYSERR_NOTSUPPORTED. This message is valid only for the <a href="https://docs.microsoft.com/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <b>waveOutMessage</b>, <a href="https://docs.microsoft.com/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="https://docs.microsoft.com/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, and <a href="https://docs.microsoft.com/previous-versions/dd757307(v=vs.85)">mixerMessage</a> functions.  The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

The <code>DRV_QUERYMAPPABLE</code> message queries for whether the specified device can be used by a mapper.

For <code>DRV_QUERYMAPPABLE</code>, <i>dwParam1</i> is unused. Set this parameter to zero.

For <code>DRV_QUERYMAPPABLE</code>, <i>dwParam2</i> is unused. Set this parameter to zero.

This message is valid only for the <a href="https://docs.microsoft.com/previous-versions/dd743846(v=vs.85)">waveInMessage</a>, <b>waveOutMessage</b>, <a href="https://docs.microsoft.com/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="https://docs.microsoft.com/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, <a href="https://docs.microsoft.com/previous-versions/dd757307(v=vs.85)">mixerMessage</a> and <a href="https://docs.microsoft.com/previous-versions/dd756716(v=vs.85)">auxOutMessage</a> functions. The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

When an application program opens a mapper instead of a specific audio device, the system inserts a mapper between the application and the available devices. The mapper selects an appropriate device by mapping the application's requirements to one of the available devices. For more information about mappers, see the Microsoft Windows SDK documentation.

The <code>DRVM_MAPPER_CONSOLEVOICECOM_GET</code> message retrieves the device ID of the preferred voice-communications device.

For <code>DRVM_MAPPER_CONSOLEVOICECOM_GET</code>, <i>dwParam1</i> is a pointer to device ID. This parameter points to a DWORD variable into which the function writes the device ID of the current preferred voice-communications device. The function writes the value (-1) if no device is available that qualifies as a preferred voice-communications device.

For <code>DRVM_MAPPER_CONSOLEVOICECOM_GET</code>, <i>dwParam2</i> is a pointer to status flags. This parameter points to a DWORD variable into which the function writes the device-status flags. Only one flag bit is currently defined: DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY. 

This message is valid only for the <a href="https://docs.microsoft.com/previous-versions/dd743846(v=vs.85)">waveInMessage</a> and <b>waveOutMessage</b> functions. When a caller calls these two functions with the DRVM_MAPPER_CONSOLEVOICECOM_GET message, the caller must specify the device ID as WAVE_MAPPER, and then cast this value to the appropriate handle type. For the <b>waveInMessage</b>, <b>waveOutMessage</b>, <a href="https://docs.microsoft.com/previous-versions/dd798457(v=vs.85)">midiInMessage</a>, <a href="https://docs.microsoft.com/previous-versions/dd798475(v=vs.85)">midiOutMessage</a>, or <a href="https://docs.microsoft.com/previous-versions/dd757307(v=vs.85)">mixerMessage</a> functions, the caller must cast the device ID to a handle of type HWAVEIN, HWAVEOUT, HMIDIIN, HMIDIOUT, or HMIXER, respectively. Note that if the caller supplies a valid handle instead of a device ID for this parameter, the function fails and returns error code MMSYSERR_NOSUPPORT.

The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

This message provides a way to determine which device is preferred specifically for voice communications, in contrast to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff536362(v=vs.85)">DRVM_MAPPER_PREFERRED_GET</a> message, which determines which device is preferred for all other audio functions.

For example, the preferred <b>waveOut</b> device for voice communications might be the earpiece in a headset, but the preferred <b>waveOut</b> device for all other audio functions might be a set of stereo speakers.

When the DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY flag bit is set in the DWORD location pointed to by <i>dwParam2</i>, the <b>waveIn</b> and <b>waveOut</b> APIs use only the current preferred voice-communications device and do not search for other available devices if the preferred device is unavailable. The flag that is output by either the <b>waveInMessage</b> or <b>waveOutMessage</b> call applies to the preferred voice-communications device for both the <b>waveIn</b> and <b>waveOut</b> APIs, regardless of whether the call is made to <b>waveInMessage</b> or <b>waveOutMessage</b>. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/preferred-voice-communications-device-id">Preferred Voice-Communications Device ID</a>.

The <code>DRVM_MAPPER_PREFERRED_GET</code> message retrieves the device ID of the preferred audio device.

For <code>DRVM_MAPPER_PREFERRED_GET</code>, <i>dwParam1</i> is a pointer to device ID. This parameter points to a DWORD variable into which the function writes the device ID of the current preferred device. The function writes the value (-1) if no device is available that qualifies as a preferred device.

For <code>DRVM_MAPPER_PREFERRED_GET</code>, <i>dwParam2</i> is a pointer to status flags. This parameter points to a DWORD variable into which the function writes the device-status flags. Only one flag bit is currently defined (for <b>waveInMessage</b> and <b>waveOutMessage</b> calls only): DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY. 

This message is valid only for the <a href="https://docs.microsoft.com/previous-versions/dd743846(v=vs.85)">waveInMessage</a>,  <b>waveOutMessage</b> and  <a href="https://docs.microsoft.com/previous-versions/dd798475(v=vs.85)">midiOutMessage</a> functions. When the caller calls these functions with the DRVM_MAPPER_PREFERRED_GET message, the caller must first specify the device ID as WAVE_MAPPER (for <b>waveInMessage</b> or <b>waveOutMessage</b>) or MIDI_MAPPER (for <b>midiOutMessage</b>), and then cast this value to the appropriate handle type. For the <b>waveInMessage</b>, <b>waveOutMessage</b>, or <b>midiOutMessage</b> functions, the caller must cast the device ID to a handle type HWAVEIN, HWAVEOUT or HMIDIOUT, respectively. Note that if the caller supplies a valid handle instead of a device ID for this parameter, the function fails and returns error code MMSYSERR_NOSUPPORT.

The system intercepts this message and returns the appropriate value without sending the message to the device driver. For general information about system-intercepted <b>xxxMessage</b> functions, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/system-intercepted-device-messages">System-Intercepted Device Messages</a>.

This message provides a way to determine which device is preferred for audio functions in general, in contrast to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff536361(v=vs.85)">DRVM_MAPPER_CONSOLEVOICECOM_GET</a> message, which determines which device is preferred specifically for voice communications.

When the DRVM_MAPPER_PREFERRED_FLAGS_PREFERREDONLY flag bit is set in the DWORD location pointed to by <i>dwParam2</i>, the <b>waveIn</b> and <b>waveOut</b> APIs use only the current preferred device and do not search for other available devices if the preferred device is unavailable. Note that the <b>midiOutMessage</b> function does not output this flag--the <b>midiOut</b> API always uses only the preferred device. The flag that is output by either the <b>waveInMessage</b> or <b>waveOutMessage</b> call applies to the preferred device for both the <b>waveIn</b> and <b>waveOut</b> APIs, regardless of whether the call is made to <b>waveInMessage</b> or <b>waveOutMessage</b>.

The <i>xxx</i>Message functions accept this value in place of a valid device handle in order to allow an application to determine the default device ID without first having to open a device. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/audio/accessing-the-preferred-device-id">Accessing the Preferred Device ID</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>
 

 

