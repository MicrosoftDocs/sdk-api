---
UID: NF:tapi3if.ITPhone.put_ButtonMode
title: ITPhone::put_ButtonMode (tapi3if.h)
description: The put_ButtonMode method sets the button mode.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","put_ButtonMode method","ITPhone.put_ButtonMode","ITPhone::put_ButtonMode","_tapi3_itphone_put_buttonmode","put_ButtonMode","put_ButtonMode method [TAPI 2.2]","put_ButtonMode method [TAPI 2.2]","ITPhone interface","tapi3.itphone_put_buttonmode","tapi3if/ITPhone::put_ButtonMode"]
old-location: tapi3\itphone_put_buttonmode.htm
tech.root: tapi3
ms.assetid: d2287c86-5884-4890-956c-fcc26c426cd3
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_ButtonMode method, ITPhone.put_ButtonMode, ITPhone::put_ButtonMode, _tapi3_itphone_put_buttonmode, put_ButtonMode, put_ButtonMode method [TAPI 2.2], put_ButtonMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_buttonmode, tapi3if/ITPhone::put_ButtonMode
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
 - ITPhone::put_ButtonMode
 - tapi3if/ITPhone::put_ButtonMode
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
 - ITPhone.put_ButtonMode
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
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_mode">PHONE_BUTTON_MODE</a> descriptor for the button's mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonmode">get_ButtonMode</a>