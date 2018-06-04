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

# _WSDUdpRetransmitParams structure


## -description


Defines the parameters for repeating a message transimission.


## -struct-fields




### -field ulSendDelay

Time to wait before sending the first transmission, in milliseconds. Specify zero for no delay. Cannot be INFINITE.


### -field ulRepeat

Maximum number of transmissions to send. Specify a value between 1 and 256, inclusively.


### -field ulRepeatMinDelay

Minimum value of the range used to generate the initial delay value, in milliseconds. This value must be less than or equal to <b>ulRepeatMaxDelay</b>, can be zero, but cannot be INFINITE. See Remarks.


### -field ulRepeatMaxDelay

Maximum value of the range used to generate the initial delay value, in milliseconds. This value be less than or equal to <b>ulRepeatUpperDelay</b>, can be zero, but cannot be INFINITE. See Remarks.


### -field ulRepeatUpperDelay

Maximum delay to wait before sending message, in milliseconds. This value be can be zero, but cannot be INFINITE.


## -remarks



If <b>ulRepeatMinDelay</b>, <b>ulRepeatMaxDelay</b>, and <b>ulRepeatUpperDelay</b> are all zero, there is no delay in retransmission of the message.

WSD sends the first transmission after waiting <b>ulSendDelay</b>. WSD uses the other members to determine when to repeat the transmission, if necessary. WSD repeats the transmission up to <b>ulRepeat</b> times with increasing delays between transmission. WSD uses the <b>ulRepeatMinDelay</b>, <b>ulRepeatMaxDelay</b>, and <b>ulRepeatUpperDelay</b> members to determine the delay. 

WSD generates a random delay value in the range <b>ulRepeatMinDelay</b> to <b>ulRepeatMaxDelay</b> and waits this amount of time before repeating the transmission. All subsequent repeat attempts then double the current delay value until <b>ulRepeatUpperDelay</b> is reached. For example, if the initial random delay value is 50 and the upper delay value is 250, the second attempt will wait 50 milliseconds, the third attempt will wait 100 milliseconds, the fourth attempt will wait 200 milliseconds, and the remaining attempts will wait 250 milliseconds.

For details on how WSD uses these values to send messages, see Appendix I of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84390">SOAP-over-UDP</a> specification.




## -see-also




<a href="https://msdn.microsoft.com/c34d6320-c70b-410e-ae21-fba849dac62f">IWSDUdpMessageParameters::GetRetransmitParams</a>



<a href="https://msdn.microsoft.com/8fef8dc9-7621-4928-94a6-491a095b11fa">IWSDUdpMessageParameters::SetRetransmitParams</a>
 

 

