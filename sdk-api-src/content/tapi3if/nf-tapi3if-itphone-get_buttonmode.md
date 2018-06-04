---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

