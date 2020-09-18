---
UID: NF:tapi3if.ITAutomatedPhoneControl.StartRinger
title: ITAutomatedPhoneControl::StartRinger (tapi3if.h)
description: The StartRinger method starts the phone's ringer, specifying the ring mode and the duration of the ring.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","StartRinger method","ITAutomatedPhoneControl.StartRinger","ITAutomatedPhoneControl::StartRinger","StartRinger","StartRinger method [TAPI 2.2]","StartRinger method [TAPI 2.2]","ITAutomatedPhoneControl interface","_tapi3_itautomatedphonecontrol_startringer","tapi3.itautomatedphonecontrol_startringer","tapi3if/ITAutomatedPhoneControl::StartRinger"]
old-location: tapi3\itautomatedphonecontrol_startringer.htm
tech.root: tapi3
ms.assetid: bf94aab7-6b12-43f8-b49f-a7cf6617dd57
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],StartRinger method, ITAutomatedPhoneControl.StartRinger, ITAutomatedPhoneControl::StartRinger, StartRinger, StartRinger method [TAPI 2.2], StartRinger method [TAPI 2.2],ITAutomatedPhoneControl interface, _tapi3_itautomatedphonecontrol_startringer, tapi3.itautomatedphonecontrol_startringer, tapi3if/ITAutomatedPhoneControl::StartRinger
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
 - ITAutomatedPhoneControl::StartRinger
 - tapi3if/ITAutomatedPhoneControl::StartRinger
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
 - ITAutomatedPhoneControl.StartRinger
---

# ITAutomatedPhoneControl::StartRinger


## -description

The 
<b>StartRinger</b> method starts the phone's ringer, specifying the ring mode and the duration of the ring.

## -parameters

### -param lRingMode [in]

Ring mode. The exact meaning of this value is device-dependent. For more information, see the following Remarks section.

### -param lDuration [in]

Length of ring.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

If you specify the value zero in the <i>lRingMode</i> parameter, and the phone doesn't have a ringer device, the 
<b>StartRinger</b> method attempts to play the ringing sound on the system's default audio render device. Examples of default devices include sound card speakers and a USB phone's audio render device. For more information, see 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_long">PHONECAPS_LONG</a>.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>