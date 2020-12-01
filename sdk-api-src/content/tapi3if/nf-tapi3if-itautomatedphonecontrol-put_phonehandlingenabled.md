---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_PhoneHandlingEnabled
title: ITAutomatedPhoneControl::put_PhoneHandlingEnabled (tapi3if.h)
description: The put_PhoneHandlingEnabled method sets the PhoneHandlingEnabled property.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_PhoneHandlingEnabled method","ITAutomatedPhoneControl.put_PhoneHandlingEnabled","ITAutomatedPhoneControl::put_PhoneHandlingEnabled","_tapi3_itautomatedphonecontrol_put_phonehandlingenabled","put_PhoneHandlingEnabled","put_PhoneHandlingEnabled method [TAPI 2.2]","put_PhoneHandlingEnabled method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_phonehandlingenabled","tapi3if/ITAutomatedPhoneControl::put_PhoneHandlingEnabled"]
old-location: tapi3\itautomatedphonecontrol_put_phonehandlingenabled.htm
tech.root: tapi3
ms.assetid: 6759b811-2fc1-4827-a03e-d19335520829
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_PhoneHandlingEnabled method, ITAutomatedPhoneControl.put_PhoneHandlingEnabled, ITAutomatedPhoneControl::put_PhoneHandlingEnabled, _tapi3_itautomatedphonecontrol_put_phonehandlingenabled, put_PhoneHandlingEnabled, put_PhoneHandlingEnabled method [TAPI 2.2], put_PhoneHandlingEnabled method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_phonehandlingenabled, tapi3if/ITAutomatedPhoneControl::put_PhoneHandlingEnabled
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
 - ITAutomatedPhoneControl::put_PhoneHandlingEnabled
 - tapi3if/ITAutomatedPhoneControl::put_PhoneHandlingEnabled
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
 - ITAutomatedPhoneControl.put_PhoneHandlingEnabled
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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a> interface (to configure the details of the automatic phone interaction features required) before setting the <b>PhoneHandlingEnabled</b> property to VARIANT_TRUE. However, you can also adjust the properties after you call the 
<b>put_PhoneHandlingEnabled</b> method to enable the features.

When the phone is closed with a call to the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-close">ITPhone::Close</a> method, the <b>PhoneHandlingEnabled</b> property is automatically reset to VARIANT_FALSE.

If you set the <b>PhoneHandlingEnabled</b> property to VARIANT_TRUE, and the phone doesn't have a ringer device, the ringing sound plays on the default audio device for the system; for example, on sound card speakers. For more information, see 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_long">PHONECAPS_LONG</a>.

For a list of property methods that get and set the automatic phone interaction features, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-close">ITPhone::Close</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_phonehandlingenabled">get_PhoneHandlingEnabled</a>