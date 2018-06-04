---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# phonestatus_tag structure


## -description


The 
<b>PHONESTATUS</b> structure describes the current status of a phone device. The 
<a href="https://msdn.microsoft.com/d2e9e209-54f5-4895-b57a-a5f4c24e063e">phoneGetStatus</a> and 
<a href="https://msdn.microsoft.com/92cf7299-2e1f-42ce-abf7-2824d993bd59">TSPI_phoneGetStatus</a> functions return this structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwStatusFlags

Status flags for this phone device. This member uses one of the 
<a href="https://msdn.microsoft.com/e94da591-49ab-4932-8621-0a62b8a55dd6">PHONESTATUSFLAGS_ Constants</a>.


### -field dwNumOwners

Number of application modules with owner privilege for the phone.


### -field dwNumMonitors

Number of application modules with monitor privilege for the phone.


### -field dwRingMode

Current ring mode of a phone device.


### -field dwRingVolume

Current ring volume of a phone device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum volume).


### -field dwHandsetHookSwitchMode

Current hookswitch mode of the phone's handset. This member uses one of the 
<a href="https://msdn.microsoft.com/532bf089-d5ca-4a04-847d-69e48990ff5c">PHONEHOOKSWITCHMODE_ Constants</a>.


### -field dwHandsetVolume

Current speaker volume of the phone's handset device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum volume).


### -field dwHandsetGain

Current microphone gain of the phone's handset device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum gain).


### -field dwSpeakerHookSwitchMode

Current hookswitch mode of the phone's speakerphone. This member uses one of the 
<a href="https://msdn.microsoft.com/532bf089-d5ca-4a04-847d-69e48990ff5c">PHONEHOOKSWITCHMODE_ Constants</a>.


### -field dwSpeakerVolume

Current speaker volume of the phone's speaker device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum volume).


### -field dwSpeakerGain

Current microphone gain of the phone's speaker device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum gain).


### -field dwHeadsetHookSwitchMode

Current hookswitch mode of the phone's headset. This member uses one of the 
<a href="https://msdn.microsoft.com/532bf089-d5ca-4a04-847d-69e48990ff5c">PHONEHOOKSWITCHMODE_ Constants</a>.


### -field dwHeadsetVolume

Current speaker volume of the phone's headset device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum volume).


### -field dwHeadsetGain

Current microphone gain of the phone's headset device. This is a value between 0x00000000 (silence) and 0x0000FFFF (maximum gain).


### -field dwDisplaySize

Size of the display information, in bytes.


### -field dwDisplayOffset

Offset from the beginning of this structure to the variably sized field containing the phone's current display information. The size of the field is specified by <b>dwDisplaySize</b>.


### -field dwLampModesSize

Size of the current lamp modes array, in bytes.


### -field dwLampModesOffset

Offset from the beginning of this structure to the variably sized field containing the phone's current lamp modes. The size of the field is specified by <b>dwLampModesSize</b>.


### -field dwOwnerNameSize

Size of the name of the current owner, including the <b>null</b> terminator, in bytes.


### -field dwOwnerNameOffset

Offset from the beginning of the structure to the variably sized field containing the name of the application that is the current owner of the phone device. The name is the application name provided by the application when it invoked with 
<a href="https://msdn.microsoft.com/e06153c1-707e-45a9-8d26-747d53e16cf2">phoneInitialize</a> or 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>. If no application name was supplied, the application's filename is used instead. The size of the field is specified by <b>dwOwnerNameSize</b>. If the phone currently has no owner, <b>dwOwnerNameSize</b> is zero.


### -field dwDevSpecificSize

Size of the device-specific field, in bytes. If the device-specific information is a pointer to a string, the size must include the <b>null</b> terminator.


### -field dwDevSpecificOffset

Offset from the beginning of this structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.


### -field dwPhoneFeatures

Flags that indicate which Telephony API functions can be invoked on the phone, considering the availability of the feature in the device capabilities, the current device state, and device ownership of the invoking application. A zero indicates the corresponding feature cannot be invoked by the application on the phone in its current state; a one indicates the feature can be invoked. This member uses one or more of the 
<a href="https://msdn.microsoft.com/361b3080-3650-48a2-a1b7-f05d72777f9a">PHONEFEATURE_ Constants</a>.


## -remarks



Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

The <b>dwPhoneFeatures</b> member is available only to applications that open the phone device with an API version of 2.0 or later.




## -see-also




<a href="https://msdn.microsoft.com/92cf7299-2e1f-42ce-abf7-2824d993bd59">TSPI_phoneGetStatus</a>



<a href="https://msdn.microsoft.com/d2e9e209-54f5-4895-b57a-a5f4c24e063e">phoneGetStatus</a>



<a href="https://msdn.microsoft.com/e06153c1-707e-45a9-8d26-747d53e16cf2">phoneInitialize</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>
 

 

