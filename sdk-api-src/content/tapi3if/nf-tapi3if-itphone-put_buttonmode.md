---
UID: NF:tapi3if.ITPhone.put_ButtonMode
title: ITPhone::put_ButtonMode
author: windows-sdk-content
description: The put_ButtonMode method sets the button mode.
old-location: tapi3\itphone_put_buttonmode.htm
tech.root: tapi
ms.assetid: d2287c86-5884-4890-956c-fcc26c426cd3
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_ButtonMode method, ITPhone.put_ButtonMode, ITPhone::put_ButtonMode, _tapi3_itphone_put_buttonmode, put_ButtonMode, put_ButtonMode method [TAPI 2.2], put_ButtonMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_buttonmode, tapi3if/ITPhone::put_ButtonMode
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
 - ITPhone.put_ButtonMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::put_ButtonMode


## -description


The 
<b>put_ButtonMode</b> method sets the button mode.


## -parameters




### -param lButtonID [in]

Button identifier.


### -param ButtonMode [in]

The 
<a href="https://msdn.microsoft.com/ae410224-bb01-4d56-95e8-1c2ead544cf1">PHONE_BUTTON_MODE</a> descriptor for the button's mode.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/5b3173bf-1c79-4c5d-a2bc-3b3ae4f0ae8a">get_ButtonMode</a>
 

 

