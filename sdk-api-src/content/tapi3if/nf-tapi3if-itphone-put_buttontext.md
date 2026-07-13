---
UID: NF:tapi3if.ITPhone.put_ButtonText
title: ITPhone::put_ButtonText (tapi3if.h)
description: The put_ButtonText method sets the button text.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","put_ButtonText method","ITPhone.put_ButtonText","ITPhone::put_ButtonText","_tapi3_itphone_put_buttontext","put_ButtonText","put_ButtonText method [TAPI 2.2]","put_ButtonText method [TAPI 2.2]","ITPhone interface","tapi3.itphone_put_buttontext","tapi3if/ITPhone::put_ButtonText"]
old-location: tapi3\itphone_put_buttontext.htm
tech.root: tapi3
ms.assetid: b50427e9-94cd-47bb-910f-2f879df9bcf8
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_ButtonText method, ITPhone.put_ButtonText, ITPhone::put_ButtonText, _tapi3_itphone_put_buttontext, put_ButtonText, put_ButtonText method [TAPI 2.2], put_ButtonText method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_buttontext, tapi3if/ITPhone::put_ButtonText
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
 - ITPhone::put_ButtonText
 - tapi3if/ITPhone::put_ButtonText
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
 - ITPhone.put_ButtonText
---

# ITPhone::put_ButtonText


## -description

The 
<b>put_ButtonText</b> method sets the button text.

## -parameters

### -param lButtonID [in]

Button identifier.

### -param bstrButtonText [in]

The <b>BSTR</b> representation of the button text.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttontext">get_ButtonText</a>