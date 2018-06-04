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

# ITAutomatedPhoneControl::put_PhoneHandlingEnabled


## -description


The 
<b>put_PhoneHandlingEnabled</b> method sets the <b>PhoneHandlingEnabled</b> property. Setting the property enables or disables all the automatic phone interaction features for this phone. Features include automated control of a phone's tones and rings, and automated call handling based on a phone's hookswitch state.


## -parameters




### -param fEnabled [in]

If VARIANT_TRUE, phone handling is enabled. If VARIANT_FALSE, phone handling is disabled. The default value is VARIANT_FALSE.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



Typically, an application sets other properties on the 
<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a> interface (to configure the details of the automatic phone interaction features required) before setting the <b>PhoneHandlingEnabled</b> property to VARIANT_TRUE. However, you can also adjust the properties after you call the 
<b>put_PhoneHandlingEnabled</b> method to enable the features.

When the phone is closed with a call to the 
<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">ITPhone::Close</a> method, the <b>PhoneHandlingEnabled</b> property is automatically reset to VARIANT_FALSE.

If you set the <b>PhoneHandlingEnabled</b> property to VARIANT_TRUE, and the phone doesn't have a ringer device, the ringing sound plays on the default audio device for the system; for example, on sound card speakers. For more information, see 
<a href="https://msdn.microsoft.com/7a73d5ff-d08a-46e6-b4ad-4f3b973967a7">PHONECAPS_LONG</a>.

For a list of property methods that get and set the automatic phone interaction features, see 
<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">ITPhone::Close</a>



<a href="https://msdn.microsoft.com/a6174caa-6045-4b82-9b13-11b86f8cf8a8">get_PhoneHandlingEnabled</a>
 

 

