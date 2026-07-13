---
UID: NF:tapi3if.ITPhone.put_LampMode
title: ITPhone::put_LampMode (tapi3if.h)
description: The put_LampMode method sets the current lamp mode for the given lamp.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","put_LampMode method","ITPhone.put_LampMode","ITPhone::put_LampMode","_tapi3_itphone_put_lampmode","put_LampMode","put_LampMode method [TAPI 2.2]","put_LampMode method [TAPI 2.2]","ITPhone interface","tapi3.itphone_put_lampmode","tapi3if/ITPhone::put_LampMode"]
old-location: tapi3\itphone_put_lampmode.htm
tech.root: tapi3
ms.assetid: 0445cf2c-1b00-4136-bdab-3c6e0669ef11
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_LampMode method, ITPhone.put_LampMode, ITPhone::put_LampMode, _tapi3_itphone_put_lampmode, put_LampMode, put_LampMode method [TAPI 2.2], put_LampMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_lampmode, tapi3if/ITPhone::put_LampMode
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
 - ITPhone::put_LampMode
 - tapi3if/ITPhone::put_LampMode
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
 - ITPhone.put_LampMode
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
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_lamp_mode">PHONE_LAMP_MODE</a> descriptor for the phone's lamp status.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_lampmode">get_LampMode</a>