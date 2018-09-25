---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_Ringer
title: ITAutomatedPhoneControl::get_Ringer
author: windows-sdk-content
description: The get_Ringer method returns a Boolean value indicating whether the phone is currently performing an incoming ring that was initiated by the StartRinger method on this interface.
old-location: tapi3\itautomatedphonecontrol_get_ringer.htm
tech.root: tapi
ms.assetid: cc4daec0-7f55-4c76-b8a0-19307c7046dc
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_Ringer method, ITAutomatedPhoneControl.get_Ringer, ITAutomatedPhoneControl::get_Ringer, _tapi3_itautomatedphonecontrol_get_ringer, get_Ringer, get_Ringer method [TAPI 2.2], get_Ringer method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_ringer, tapi3if/ITAutomatedPhoneControl::get_Ringer
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
 - ITAutomatedPhoneControl.get_Ringer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::get_Ringer


## -description


The 
<b>get_Ringer</b> method returns a Boolean value indicating whether the phone is currently performing an incoming ring that was initiated by the 
<a href="https://msdn.microsoft.com/bf94aab7-6b12-43f8-b49f-a7cf6617dd57">StartRinger</a> method on this interface.


## -parameters




### -param pfRinging [out]

If VARIANT_TRUE, the phone is currently ringing.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/bf94aab7-6b12-43f8-b49f-a7cf6617dd57">StartRinger</a>
 

 

