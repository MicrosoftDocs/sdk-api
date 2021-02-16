---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoKeypadTonesMinimumDuration
title: ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration (tapi3if.h)
description: The put_AutoKeypadTonesMinimumDuration method sets the value of the AutoKeypadTonesMinimumDuration property. The property specifies how long to play keypad tones on PBS_DOWN.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoKeypadTonesMinimumDuration method","ITAutomatedPhoneControl.put_AutoKeypadTonesMinimumDuration","ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration","_tapi3_itautomatedphonecontrol_put_autokeypadtonesminimumduration","put_AutoKeypadTonesMinimumDuration","put_AutoKeypadTonesMinimumDuration method [TAPI 2.2]","put_AutoKeypadTonesMinimumDuration method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autokeypadtonesminimumduration","tapi3if/ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration"]
old-location: tapi3\itautomatedphonecontrol_put_autokeypadtonesminimumduration.htm
tech.root: tapi3
ms.assetid: 8c4bdd45-7d19-47a4-aa18-5944d3e58797
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoKeypadTonesMinimumDuration method, ITAutomatedPhoneControl.put_AutoKeypadTonesMinimumDuration, ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration, _tapi3_itautomatedphonecontrol_put_autokeypadtonesminimumduration, put_AutoKeypadTonesMinimumDuration, put_AutoKeypadTonesMinimumDuration method [TAPI 2.2], put_AutoKeypadTonesMinimumDuration method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autokeypadtonesminimumduration, tapi3if/ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration
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
 - ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration
 - tapi3if/ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration
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
 - ITAutomatedPhoneControl.put_AutoKeypadTonesMinimumDuration
---

# ITAutomatedPhoneControl::put_AutoKeypadTonesMinimumDuration


## -description

The 
<b>put_AutoKeypadTonesMinimumDuration</b> method sets the value of the <b>AutoKeypadTonesMinimumDuration</b> property. The property specifies how long to play keypad tones on PBS_DOWN.

## -parameters

### -param lDuration [in]

Minimum duration of keypad tones, in milliseconds (ms). The default value is 250 ms. If the minimum duration elapses without a PBS_UP event, the keypad tone continues until the PBS_UP event is received.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoKeypadTonesMinimumDuration</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autokeypadtonesminimumduration">get_AutoKeypadTonesMinimumDuration</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>