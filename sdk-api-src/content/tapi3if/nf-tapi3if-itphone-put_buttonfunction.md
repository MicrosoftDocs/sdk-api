---
UID: NF:tapi3if.ITPhone.put_ButtonFunction
title: ITPhone::put_ButtonFunction
author: windows-sdk-content
description: The put_ButtonFunction method sets the button function.
old-location: tapi3\itphone_put_buttonfunction.htm
tech.root: tapi
ms.assetid: 8002ab8a-a15d-4a1f-b0c3-7a15c61cb6c4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_ButtonFunction method, ITPhone.put_ButtonFunction, ITPhone::put_ButtonFunction, _tapi3_itphone_put_buttonfunction, put_ButtonFunction, put_ButtonFunction method [TAPI 2.2], put_ButtonFunction method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_buttonfunction, tapi3if/ITPhone::put_ButtonFunction
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
 - ITPhone.put_ButtonFunction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::put_ButtonFunction


## -description


The 
<b>put_ButtonFunction</b> method sets the button function.


## -parameters




### -param lButtonID [in]

Button identifier.


### -param ButtonFunction [in]

The 
<a href="https://msdn.microsoft.com/2200b9aa-37fb-483f-9bfa-928348a4bc51">PHONE_BUTTON_FUNCTION</a> descriptor for the button's function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/a884c0b4-141a-4f04-8cfb-7ae6b1ec11b3">get_ButtonFunction</a>
 

 

