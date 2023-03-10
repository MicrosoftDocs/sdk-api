---
UID: NF:tapi3if.ITPhone.get_LampMode
title: ITPhone::get_LampMode (tapi3if.h)
description: The get_LampMode method gets the current lamp mode for the given lamp.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_LampMode method","ITPhone.get_LampMode","ITPhone::get_LampMode","_tapi3_itphone_get_lampmode","get_LampMode","get_LampMode method [TAPI 2.2]","get_LampMode method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_lampmode","tapi3if/ITPhone::get_LampMode"]
old-location: tapi3\itphone_get_lampmode.htm
tech.root: tapi3
ms.assetid: 5e0fa135-304a-4598-a6cd-2e5734b3678c
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_LampMode method, ITPhone.get_LampMode, ITPhone::get_LampMode, _tapi3_itphone_get_lampmode, get_LampMode, get_LampMode method [TAPI 2.2], get_LampMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_lampmode, tapi3if/ITPhone::get_LampMode
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
 - ITPhone::get_LampMode
 - tapi3if/ITPhone::get_LampMode
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
 - ITPhone.get_LampMode
---

# ITPhone::get_LampMode


## -description

The 
<b>get_LampMode</b> method gets the current lamp mode for the given lamp.

## -parameters

### -param lLampID [in]

Lamp identifier.

### -param pLampMode [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_lamp_mode">PHONE_LAMP_MODE</a> descriptor for the phone's lamp status.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_lampmode">put_LampMode</a>