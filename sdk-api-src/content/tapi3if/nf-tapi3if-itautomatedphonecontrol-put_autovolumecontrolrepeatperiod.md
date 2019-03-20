---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoVolumeControlRepeatPeriod
title: ITAutomatedPhoneControl::put_AutoVolumeControlRepeatPeriod (tapi3if.h)
author: windows-sdk-content
description: The put_AutoVolumeControlRepeatPeriod method sets the AutoVolumeControlRepeatPeriod property. The property controls the period, in milliseconds (ms), of button repeats when a volume button is held down.
old-location: tapi3\itautomatedphonecontrol_put_autovolumecontrolrepeatperiod.htm
tech.root: Tapi
ms.assetid: 932b1092-6396-4ee9-84d7-1e28b09d132f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoVolumeControlRepeatPeriod method, ITAutomatedPhoneControl.put_AutoVolumeControlRepeatPeriod, ITAutomatedPhoneControl::put_AutoVolumeControlRepeatPeriod, _tapi3_itautomatedphonecontrol_put_autovolumecontrolrepeatperiod, put_AutoVolumeControlRepeatPeriod, put_AutoVolumeControlRepeatPeriod method [TAPI 2.2], put_AutoVolumeControlRepeatPeriod method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autovolumecontrolrepeatperiod, tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlRepeatPeriod
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
 - ITAutomatedPhoneControl.put_AutoVolumeControlRepeatPeriod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::put_AutoVolumeControlRepeatPeriod


## -description


The 
<b>put_AutoVolumeControlRepeatPeriod</b> method sets the <b>AutoVolumeControlRepeatPeriod</b> property. The property controls the period, in milliseconds (ms), of button repeats when a volume button is held down.


## -parameters




### -param lPeriod [in]

Period, in milliseconds (ms), of button repeats when a volume button is held down. The default value is 100 ms.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/6ab52127-62e2-4e80-980a-8b29b51fa91f">get_AutoVolumeControlRepeatPeriod</a>



<a href="https://msdn.microsoft.com/5a57c0ef-440a-4939-8d15-edb0c59dc1a4">put_AutoKeypadTones</a>
 

 

