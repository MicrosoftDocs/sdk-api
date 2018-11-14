---
UID: NF:tapi3if.ITPhone.get_Display
title: ITPhone::get_Display
author: windows-sdk-content
description: The get_Display method gets the display for the phone. In TAPI, the display is simply an NxM character buffer.
old-location: tapi3\itphone_get_display.htm
tech.root: tapi
ms.assetid: 259982d7-8c28-4c0d-81b3-e4ec49fc9765
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Display method, ITPhone.get_Display, ITPhone::get_Display, _tapi3_itphone_get_display, get_Display, get_Display method [TAPI 2.2], get_Display method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_display, tapi3if/ITPhone::get_Display
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
 - ITPhone.get_Display
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITPhone.get_Display
: 
---

# ITPhone::get_Display


## -description


The 
<b>get_Display</b> method gets the display for the phone. In TAPI, the display is simply an NxM character buffer.


## -parameters




### -param pbstrDisplay [out]

The <b>BSTR</b> representation of the phone display. The <b>BSTR</b> is allocated using 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/690756c4-201d-472d-b536-452074226701">SetDisplay</a>
 

 

