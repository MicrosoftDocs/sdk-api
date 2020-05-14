---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoVolumeControlStep
title: ITAutomatedPhoneControl::put_AutoVolumeControlStep (tapi3if.h)
description: The put_AutoVolumeControlStep method sets the AutoVolumeControlStep property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoVolumeControlStep method","ITAutomatedPhoneControl.put_AutoVolumeControlStep","ITAutomatedPhoneControl::put_AutoVolumeControlStep","_tapi3_itautomatedphonecontrol_put_autovolumecontrolstep","put_AutoVolumeControlStep","put_AutoVolumeControlStep method [TAPI 2.2]","put_AutoVolumeControlStep method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autovolumecontrolstep","tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlStep"]
old-location: tapi3\itautomatedphonecontrol_put_autovolumecontrolstep.htm
tech.root: Tapi
ms.assetid: 19766507-7a15-4c45-91bd-4b49ceb177e6
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoVolumeControlStep method, ITAutomatedPhoneControl.put_AutoVolumeControlStep, ITAutomatedPhoneControl::put_AutoVolumeControlStep, _tapi3_itautomatedphonecontrol_put_autovolumecontrolstep, put_AutoVolumeControlStep, put_AutoVolumeControlStep method [TAPI 2.2], put_AutoVolumeControlStep method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autovolumecontrolstep, tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlStep
f1_keywords:
- tapi3if/ITAutomatedPhoneControl.put_AutoVolumeControlStep
dev_langs:
- c++
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
- ITAutomatedPhoneControl.put_AutoVolumeControlStep
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAutomatedPhoneControl::put_AutoVolumeControlStep


## -description


The 
<b>put_AutoVolumeControlStep</b> method sets the <b>AutoVolumeControlStep</b> property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.


## -parameters




### -param lStepSize [in]

Volume control step, in milliseconds. The default value of the <b>AutoVolumeControlStep</b> property is 4096.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrolstep">get_AutoVolumeControlStep</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>
 

 

