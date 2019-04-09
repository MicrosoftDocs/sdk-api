---
UID: NF:tapi3if.ITPhone.get_ButtonState
title: ITPhone::get_ButtonState (tapi3if.h)
author: windows-sdk-content
description: The get_ButtonState method retrieves the button state associated with a particular button.
old-location: tapi3\itphone_get_buttonstate.htm
tech.root: Tapi
ms.assetid: f14e0593-0f03-4119-b80a-12d32b68aa99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonState method, ITPhone.get_ButtonState, ITPhone::get_ButtonState, _tapi3_itphone_get_buttonstate, get_ButtonState, get_ButtonState method [TAPI 2.2], get_ButtonState method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttonstate, tapi3if/ITPhone::get_ButtonState
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
 - ITPhone.get_ButtonState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_ButtonState


## -description


The 
<b>get_ButtonState</b> method retrieves the button state associated with a particular button.

The application must call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before invoking this method; otherwise, the invocation fails.


## -parameters




### -param lButtonID [in]

Button identifier.


### -param pButtonState [out]

The 
<a href="https://msdn.microsoft.com/a9f7b527-9c74-45ac-9394-6f736aae1ccf">PHONE_BUTTON_STATE</a> descriptor for the button's state.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/6eedda9d-c127-446d-972c-09a7c1a4bd0f">ITPhoneEvent::get_ButtonState</a>
 

 

