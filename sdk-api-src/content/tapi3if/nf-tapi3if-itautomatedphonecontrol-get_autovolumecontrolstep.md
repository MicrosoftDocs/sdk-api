---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControlStep
title: ITAutomatedPhoneControl::get_AutoVolumeControlStep (tapi3if.h)
description: The get_AutoVolumeControlStep method retrieves the current value of the AutoVolumeControlStep property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoVolumeControlStep method","ITAutomatedPhoneControl.get_AutoVolumeControlStep","ITAutomatedPhoneControl::get_AutoVolumeControlStep","_tapi3_itautomatedphonecontrol_get_autovolumecontrolstep","get_AutoVolumeControlStep","get_AutoVolumeControlStep method [TAPI 2.2]","get_AutoVolumeControlStep method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autovolumecontrolstep","tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlStep"]
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrolstep.htm
tech.root: tapi3
ms.assetid: 6cf6beba-36ca-417b-91b4-9c008a14efef
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControlStep method, ITAutomatedPhoneControl.get_AutoVolumeControlStep, ITAutomatedPhoneControl::get_AutoVolumeControlStep, _tapi3_itautomatedphonecontrol_get_autovolumecontrolstep, get_AutoVolumeControlStep, get_AutoVolumeControlStep method [TAPI 2.2], get_AutoVolumeControlStep method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrolstep, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlStep
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAutomatedPhoneControl::get_AutoVolumeControlStep
 - tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlStep
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.get_AutoVolumeControlStep
---

# ITAutomatedPhoneControl::get_AutoVolumeControlStep


## -description

The 
<b>get_AutoVolumeControlStep</b> method retrieves the current value of the <b>AutoVolumeControlStep</b> property. The property determines the amount that the phone volume is adjusted when the volume button is pressed.

## -parameters

### -param plStepSize [out]

Volume control step. The default value of the <b>AutoVolumeControlStep</b> property is 4096.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolstep">put_AutoVolumeControlStep</a>