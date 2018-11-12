---
UID: NF:tapi.phoneSetHookSwitch
title: phoneSetHookSwitch function
author: windows-sdk-content
description: The phoneSetHookSwitch function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.
old-location: tapi2\phonesethookswitch.htm
tech.root: tapi
ms.assetid: 048f98e3-ac1b-47f8-85c8-97e7b7690030
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_phonesethookswitch, phoneSetHookSwitch, phoneSetHookSwitch function [TAPI 2.2], tapi/phoneSetHookSwitch, tapi2.phonesethookswitch"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneSetHookSwitch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# phoneSetHookSwitch function


## -description


The 
<b>phoneSetHookSwitch</b> function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwHookSwitchDevs

Device whose hookswitch mode is to be set. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>. 







#### PHONEHOOKSWITCHDEV_HANDSET

The phone's handset.



#### PHONEHOOKSWITCHDEV_SPEAKER

The phone's speakerphone or adjunct.



#### PHONEHOOKSWITCHDEV_HEADSET

The phone's headset.


### -param dwHookSwitchMode

Hookswitch mode to set. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/532bf089-d5ca-4a04-847d-69e48990ff5c">PHONEHOOKSWITCHMODE_ Constants</a>. 







#### PHONEHOOKSWITCHMODE_ONHOOK

The device's microphone and speaker are both onhook.



#### PHONEHOOKSWITCHMODE_MIC

The device's microphone is active, the speaker is mute.



#### PHONEHOOKSWITCHMODE_SPEAKER

The device's speaker is active, the microphone is mute.



#### PHONEHOOKSWITCHMODE_MICSPEAKER

The device's microphone and speaker are both active.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALHOOKSWITCHMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_UNINITIALIZED.




## -remarks



The hookswitch mode is the same for all specified devices. If different settings are desired, this function can be invoked multiple times with a different set of parameters. A 
<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a> message is sent to the application after the hookswitch state has changed.




## -see-also




<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

