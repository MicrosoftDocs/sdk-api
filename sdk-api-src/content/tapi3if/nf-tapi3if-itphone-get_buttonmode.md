---
UID: NF:tapi3if.ITPhone.get_ButtonMode
title: ITPhone::get_ButtonMode (tapi3if.h)
author: windows-sdk-content
description: The get_ButtonMode method retrieves the button mode associated with a particular button.
old-location: tapi3\itphone_get_buttonmode.htm
tech.root: Tapi
ms.assetid: 5b3173bf-1c79-4c5d-a2bc-3b3ae4f0ae8a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonMode method, ITPhone.get_ButtonMode, ITPhone::get_ButtonMode, _tapi3_itphone_get_buttonmode, get_ButtonMode, get_ButtonMode method [TAPI 2.2], get_ButtonMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttonmode, tapi3if/ITPhone::get_ButtonMode
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
 - ITPhone.get_ButtonMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone::get_ButtonMode


## -description


The 
<b>get_ButtonMode</b> method retrieves the button mode associated with a particular button.

The application must call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param lButtonID [in]

Button identifier. For more information, see the following Remarks section.


### -param pButtonMode [out]

The 
<a href="https://msdn.microsoft.com/ae410224-bb01-4d56-95e8-1c2ead544cf1">PHONE_BUTTON_MODE</a> descriptor for the button's mode.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See the description of the 
<a href="https://msdn.microsoft.com/ae410224-bb01-4d56-95e8-1c2ead544cf1">PHONE_BUTTON_MODE</a> enum and the TAPI 2.<i>x</i> documentation for more information about button modes.

The two following 
<a href="https://msdn.microsoft.com/ae410224-bb01-4d56-95e8-1c2ead544cf1">PHONE_BUTTON_MODE</a> values are of particular interest:

<ol>
<li>If the 
<a href="https://msdn.microsoft.com/ae410224-bb01-4d56-95e8-1c2ead544cf1">PHONE_BUTTON_MODE</a> value is PBM_FEATURE, the application should call the 
<a href="https://msdn.microsoft.com/a884c0b4-141a-4f04-8cfb-7ae6b1ec11b3">get_ButtonFunction</a> to retrieve the specific meaning of the button.</li>
<li>If the 
<a href="https://msdn.microsoft.com/ae410224-bb01-4d56-95e8-1c2ead544cf1">PHONE_BUTTON_MODE</a> value is PBM_KEYPAD, the button is a keypad button whose value is indicated by the value of the <i>lButtonID</i> parameter. For example, if <i>lButtonID</i> == 10 then the button is the * (star) key on the keypad.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/a884c0b4-141a-4f04-8cfb-7ae6b1ec11b3">get_ButtonFunction</a>



<a href="https://msdn.microsoft.com/d2287c86-5884-4890-956c-fcc26c426cd3">put_ButtonMode</a>
 

 

