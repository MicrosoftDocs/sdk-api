---
UID: NF:tapi3if.ITPhone.put_LampMode
title: ITPhone::put_LampMode (tapi3if.h)
author: windows-sdk-content
description: The put_LampMode method sets the current lamp mode for the given lamp.
old-location: tapi3\itphone_put_lampmode.htm
tech.root: Tapi
ms.assetid: 0445cf2c-1b00-4136-bdab-3c6e0669ef11
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_LampMode method, ITPhone.put_LampMode, ITPhone::put_LampMode, _tapi3_itphone_put_lampmode, put_LampMode, put_LampMode method [TAPI 2.2], put_LampMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_lampmode, tapi3if/ITPhone::put_LampMode
ms.topic: method
f1_keywords: 
 - "tapi3if/ITPhone.put_LampMode"
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
 - ITPhone.put_LampMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone::put_LampMode


## -description


The 
<b>put_LampMode</b> method sets the current lamp mode for the given lamp.


## -parameters




### -param lLampID [in]

Lamp identifier.


### -param LampMode [in]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_lamp_mode">PHONE_LAMP_MODE</a> descriptor for the phone's lamp status.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_lampmode">get_LampMode</a>
 

 

