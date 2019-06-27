---
UID: NF:tapi3if.ITPhone.put_HookSwitchState
title: ITPhone::put_HookSwitchState (tapi3if.h)
author: windows-sdk-content
description: The put_HookSwitchState method sets the current hookswitch state for a particular hookswitch device on the phone.
old-location: tapi3\itphone_put_hookswitchstate.htm
tech.root: Tapi
ms.assetid: ab0bcd30-6985-4f53-a39d-90230421b6f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_HookSwitchState method, ITPhone.put_HookSwitchState, ITPhone::put_HookSwitchState, _tapi3_itphone_put_hookswitchstate, put_HookSwitchState, put_HookSwitchState method [TAPI 2.2], put_HookSwitchState method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_hookswitchstate, tapi3if/ITPhone::put_HookSwitchState
ms.topic: method
f1_keywords: 
 - "tapi3if/ITPhone.put_HookSwitchState"
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
 - ITPhone.put_HookSwitchState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone::put_HookSwitchState


## -description


The 
<b>put_HookSwitchState</b> method sets the current hookswitch state for a particular hookswitch device on the phone.

The application must call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param HookSwitchDevice [in]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_device">PHONE_HOOK_SWITCH_DEVICE</a> descriptor for the hookswitch type.


### -param HookSwitchState [in]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_state">PHONE_HOOK_SWITCH_STATE</a> descriptor for the hookswitch status.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Typically, speakerphones and headsets have application-settable hookswitch states, and handsets do not, but this feature is TSP-dependent.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_hookswitchstate">get_HookSwitchState</a>
 

 

