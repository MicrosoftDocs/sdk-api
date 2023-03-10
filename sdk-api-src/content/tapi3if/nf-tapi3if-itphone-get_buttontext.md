---
UID: NF:tapi3if.ITPhone.get_ButtonText
title: ITPhone::get_ButtonText (tapi3if.h)
description: The get_ButtonText method retrieves the button text associated with a particular button.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_ButtonText method","ITPhone.get_ButtonText","ITPhone::get_ButtonText","_tapi3_itphone_get_buttontext","get_ButtonText","get_ButtonText method [TAPI 2.2]","get_ButtonText method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_buttontext","tapi3if/ITPhone::get_ButtonText"]
old-location: tapi3\itphone_get_buttontext.htm
tech.root: tapi3
ms.assetid: 75a216fb-7bb3-4178-baa5-8ba478bd5422
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonText method, ITPhone.get_ButtonText, ITPhone::get_ButtonText, _tapi3_itphone_get_buttontext, get_ButtonText, get_ButtonText method [TAPI 2.2], get_ButtonText method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttontext, tapi3if/ITPhone::get_ButtonText
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
 - ITPhone::get_ButtonText
 - tapi3if/ITPhone::get_ButtonText
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
 - ITPhone.get_ButtonText
---

# ITPhone::get_ButtonText


## -description

The 
<b>get_ButtonText</b> method retrieves the button text associated with a particular button.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails. See the TAPI 2.<i>x</i> documentation for more information about the concept of button text.

## -parameters

### -param lButtonID [in]

Button identifier.

### -param ppButtonText [out]

The <b>BSTR</b> representation of the button text. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttontext">put_ButtonText</a>