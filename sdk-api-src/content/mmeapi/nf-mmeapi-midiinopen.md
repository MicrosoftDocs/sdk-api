---
UID: NF:mmeapi.midiInOpen
title: midiInOpen function
author: windows-sdk-content
description: The midiInOpen function opens a specified MIDI input device.
old-location: multimedia\midiinopen.htm
tech.root: Multimedia
ms.assetid: 230deaef-9473-426f-a0eb-14e259600e68
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "_win32_midiInOpen, midiInOpen, midiInOpen function [Windows Multimedia], mmeapi/midiInOpen, multimedia.midiinopen"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - midiInOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiInOpen function


## -description



The <b>midiInOpen</b> function opens a specified MIDI input device.




## -parameters




### -param phmi

Pointer to an <b>HMIDIIN</b> handle. This location is filled with a handle identifying the opened MIDI input device. The handle is used to identify the device in calls to other MIDI input functions.
          


### -param uDeviceID

Identifier of the MIDI input device to be opened.
          


### -param dwCallback

Pointer to a callback function, a thread identifier, or a handle of a window called with information about incoming MIDI messages. For more information on the callback function, see <a href="https://msdn.microsoft.com/4b33f79f-58f0-4f12-a4ee-bd3351c25aaf">MidiInProc</a>.
          


### -param dwInstance

User instance data passed to the callback function. This parameter is not used with window callback functions or threads.
          


### -param fdwOpen

Callback flag for opening the device and, optionally, a status flag that helps regulate rapid data transfers. It can be the following values.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>CALLBACK_FUNCTION</td>
<td>The <i>dwCallback</i> parameter is a callback procedure address.</td>
</tr>
<tr>
<td>CALLBACK_NULL</td>
<td>There is no callback mechanism. This value is the default setting.</td>
</tr>
<tr>
<td>CALLBACK_THREAD</td>
<td>The <i>dwCallback</i> parameter is a thread identifier.</td>
</tr>
<tr>
<td>CALLBACK_WINDOW</td>
<td>The <i>dwCallback</i> parameter is a window handle.</td>
</tr>
<tr>
<td>MIDI_IO_STATUS</td>
<td>When this parameter also specifies CALLBACK_FUNCTION, <a href="https://msdn.microsoft.com/74ed46ab-a18e-4df5-bf36-ab3dec7fafa5">MIM_MOREDATA</a> messages are sent to the callback function as well as <a href="https://msdn.microsoft.com/966aab84-420a-42ce-9989-da5910ced9c0">MIM_DATA</a> messages. Or, if this parameter also specifies CALLBACK_WINDOW, <a href="https://msdn.microsoft.com/25d507f9-01d4-4a9a-afdd-693d74e3bd22">MM_MIM_MOREDATA</a> messages are sent to the window as well as <a href="https://msdn.microsoft.com/9c580e48-78f3-4914-bdea-393823fb8482">MM_MIM_DATA</a> messages. This flag does not affect event or thread callbacks.</td>
</tr>
</table>
 

Most applications that use a callback mechanism will specify CALLBACK_FUNCTION for this parameter.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following/

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ALLOCATED</b></dt>
</dl>
</td>
<td width="60%">
The specified resource is already allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
The specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
The flags specified by <i>dwFlags</i> are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer or structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
</table>
 




## -remarks



To determine the number of MIDI input devices present in the system, use the <a href="https://msdn.microsoft.com/23303bb2-e053-4a19-a63a-4e017b861af6">midiInGetNumDevs</a> function. The device identifier specified by <i>wDeviceID</i> varies from zero to one less than the number of devices present.

If a window or thread is chosen to receive callback information, the following messages are sent to the window procedure or thread to indicate the progress of MIDI input: <a href="https://msdn.microsoft.com/8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc">MM_MIM_OPEN</a>, <a href="https://msdn.microsoft.com/261021aa-4df6-44d8-aad3-5f98b1213459">MM_MIM_CLOSE</a>, <a href="https://msdn.microsoft.com/9c580e48-78f3-4914-bdea-393823fb8482">MM_MIM_DATA</a>, <a href="https://msdn.microsoft.com/72b9eade-4224-436f-bfef-32204eaf51ae">MM_MIM_LONGDATA</a>, <a href="https://msdn.microsoft.com/03760bfc-a4ef-48cd-97a9-1b93b56fc641">MM_MIM_ERROR</a>, <a href="https://msdn.microsoft.com/2de4c2f8-2ded-4994-934c-6e72c95637b2">MM_MIM_LONGERROR</a>, and <a href="https://msdn.microsoft.com/25d507f9-01d4-4a9a-afdd-693d74e3bd22">MM_MIM_MOREDATA</a>.

If a function is chosen to receive callback information, the following messages are sent to the function to indicate the progress of MIDI input: <a href="https://msdn.microsoft.com/c7a8b856-aedd-457d-8a21-0ec2e9303960">MIM_OPEN</a>, <a href="https://msdn.microsoft.com/c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15">MIM_CLOSE</a>, <a href="https://msdn.microsoft.com/966aab84-420a-42ce-9989-da5910ced9c0">MIM_DATA</a>, <a href="https://msdn.microsoft.com/3a11ed21-e7c5-4b78-9536-f0d862e26a02">MIM_LONGDATA</a>, <a href="https://msdn.microsoft.com/ea720da5-1f18-4d0d-ac9d-45cd1c3219d6">MIM_ERROR</a>, <a href="https://msdn.microsoft.com/7e3b0716-33c4-449c-a200-e5ba72428dc1">MIM_LONGERROR</a>, and <a href="https://msdn.microsoft.com/74ed46ab-a18e-4df5-bf36-ab3dec7fafa5">MIM_MOREDATA</a>.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

