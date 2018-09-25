---
UID: NF:tapi3if.ITPhone.get_HookSwitchState
title: ITPhone::get_HookSwitchState
author: windows-sdk-content
description: The get_HookSwitchState method retrieves the current hookswitch state for a particular hookswitch device on the phone.
old-location: tapi3\itphone_get_hookswitchstate.htm
tech.root: tapi
ms.assetid: 4560b447-45af-482a-b97b-dd0cbdb52466
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_HookSwitchState method, ITPhone.get_HookSwitchState, ITPhone::get_HookSwitchState, _tapi3_itphone_get_hookswitchstate, get_HookSwitchState, get_HookSwitchState method [TAPI 2.2], get_HookSwitchState method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_hookswitchstate, tapi3if/ITPhone::get_HookSwitchState
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
 - ITPhone.get_HookSwitchState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_HookSwitchState


## -description


The 
<b>get_HookSwitchState</b> method retrieves the current hookswitch state for a particular hookswitch device on the phone.

The application must call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param HookSwitchDevice [in]

The 
<a href="https://msdn.microsoft.com/20b17e2f-f745-41ef-91ac-d2ab21d43695">PHONE_HOOK_SWITCH_DEVICE</a> descriptor for the hookswitch type.


### -param pHookSwitchState [out]

The 
<a href="https://msdn.microsoft.com/c9501a3f-1aaa-4d58-aca1-5ef00c31d195">PHONE_HOOK_SWITCH_STATE</a> descriptor for the hookswitch status.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/ab0bcd30-6985-4f53-a39d-90230421b6f4">put_HookSwitchState</a>
 

 

