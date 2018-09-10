---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_PhoneHandlingEnabled
title: ITAutomatedPhoneControl::get_PhoneHandlingEnabled
author: windows-sdk-content
description: The get_PhoneHandlingEnabled method retrieves the current value of the PhoneHandlingEnabled property.
old-location: tapi3\itautomatedphonecontrol_get_phonehandlingenabled.htm
tech.root: tapi
ms.assetid: a6174caa-6045-4b82-9b13-11b86f8cf8a8
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_PhoneHandlingEnabled method, ITAutomatedPhoneControl.get_PhoneHandlingEnabled, ITAutomatedPhoneControl::get_PhoneHandlingEnabled, _tapi3_itautomatedphonecontrol_get_phonehandlingenabled, get_PhoneHandlingEnabled, get_PhoneHandlingEnabled method [TAPI 2.2], get_PhoneHandlingEnabled method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_phonehandlingenabled, tapi3if/ITAutomatedPhoneControl::get_PhoneHandlingEnabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.get_PhoneHandlingEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::get_PhoneHandlingEnabled


## -description


The 
<b>get_PhoneHandlingEnabled</b> method retrieves the current value of the <b>PhoneHandlingEnabled</b> property. Setting the property enables or disables all the automatic phone interaction features for this phone. Features include automated control of a phone's tones and rings, and automated call handling based on a phone's hookswitch state.


## -parameters




### -param pfEnabled [out]

VARIANT_TRUE if automated phone handling is enabled, VARIANT_FALSE if automated phone handling is not enabled. The default value is VARIANT_FALSE.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



Typically, an application sets other properties on the 
<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a> interface (to configure the details of the automatic phone interaction features required) before setting the <b>PhoneHandlingEnabled</b> property to VARIANT_TRUE. However, you can also adjust the properties after you call the 
<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a> method to enable the features.

When the phone is closed with a call to the 
<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">ITPhone::Close</a> method, the <b>PhoneHandlingEnabled</b> property is automatically reset to VARIANT_FALSE.

For a list of property methods that get and set the automatic phone interaction features, see 
<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">ITPhone::Close</a>



<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
 

 

