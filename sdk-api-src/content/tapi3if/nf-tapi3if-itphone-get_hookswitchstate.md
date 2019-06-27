---
UID: NF:tapi3if.ITPhone.get_HookSwitchState
title: ITPhone::get_HookSwitchState (tapi3if.h)
author: windows-sdk-content
description: The get_HookSwitchState method retrieves the current hookswitch state for a particular hookswitch device on the phone.
old-location: tapi3\itphone_get_hookswitchstate.htm
tech.root: Tapi
ms.assetid: 4560b447-45af-482a-b97b-dd0cbdb52466
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_HookSwitchState method, ITPhone.get_HookSwitchState, ITPhone::get_HookSwitchState, _tapi3_itphone_get_hookswitchstate, get_HookSwitchState, get_HookSwitchState method [TAPI 2.2], get_HookSwitchState method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_hookswitchstate, tapi3if/ITPhone::get_HookSwitchState
ms.topic: method
f1_keywords: 
 - "tapi3if/ITPhone.get_HookSwitchState"
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
 - ITPhone.get_HookSwitchState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone::get_HookSwitchState


## -description


The 
<b>get_HookSwitchState</b> method retrieves the current hookswitch state for a particular hookswitch device on the phone.

The application must call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param HookSwitchDevice [in]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_device">PHONE_HOOK_SWITCH_DEVICE</a> descriptor for the hookswitch type.


### -param pHookSwitchState [out]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_state">PHONE_HOOK_SWITCH_STATE</a> descriptor for the hookswitch status.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_hookswitchstate">put_HookSwitchState</a>
 

 

