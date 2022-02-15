---
UID: NF:tapi3if.ITPhone.get_Display
title: ITPhone::get_Display (tapi3if.h)
description: The get_Display method gets the display for the phone. In TAPI, the display is simply an NxM character buffer.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_Display method","ITPhone.get_Display","ITPhone::get_Display","_tapi3_itphone_get_display","get_Display","get_Display method [TAPI 2.2]","get_Display method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_display","tapi3if/ITPhone::get_Display"]
old-location: tapi3\itphone_get_display.htm
tech.root: tapi3
ms.assetid: 259982d7-8c28-4c0d-81b3-e4ec49fc9765
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Display method, ITPhone.get_Display, ITPhone::get_Display, _tapi3_itphone_get_display, get_Display, get_Display method [TAPI 2.2], get_Display method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_display, tapi3if/ITPhone::get_Display
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
 - ITPhone::get_Display
 - tapi3if/ITPhone::get_Display
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
 - ITPhone.get_Display
---

# ITPhone::get_Display


## -description

The 
<b>get_Display</b> method gets the display for the phone. In TAPI, the display is simply an NxM character buffer.

## -parameters

### -param pbstrDisplay [out]

The <b>BSTR</b> representation of the phone display. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-setdisplay">SetDisplay</a>