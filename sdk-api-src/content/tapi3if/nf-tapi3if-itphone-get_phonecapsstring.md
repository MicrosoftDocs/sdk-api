---
UID: NF:tapi3if.ITPhone.get_PhoneCapsString
title: ITPhone::get_PhoneCapsString
author: windows-sdk-content
description: The get_PhoneCapsString method gets a string capability/information about the phone, based on the PHONECAPS_STRING enum passed in. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_get_phonecapsstring.htm
tech.root: Tapi
ms.assetid: e4a0ed77-455e-428c-a3e5-cd467e47b5b2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PhoneCapsString method, ITPhone.get_PhoneCapsString, ITPhone::get_PhoneCapsString, _tapi3_itphone_get_phonecapsstring, get_PhoneCapsString, get_PhoneCapsString method [TAPI 2.2], get_PhoneCapsString method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_phonecapsstring, tapi3if/ITPhone::get_PhoneCapsString
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
 - ITPhone.get_PhoneCapsString
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
- ITPhone.get_PhoneCapsString
: 
---

# ITPhone::get_PhoneCapsString


## -description


The 
<b>get_PhoneCapsString</b> method gets a string capability/information about the phone, based on the 
<a href="https://msdn.microsoft.com/3ff60aa8-9a77-48a1-a60f-1e1d31653728">PHONECAPS_STRING</a> enum passed in. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.


## -parameters




### -param pcsCap [in]

The 
<a href="https://msdn.microsoft.com/3ff60aa8-9a77-48a1-a60f-1e1d31653728">PHONECAPS_STRING</a> descriptor for the phone capability.


### -param ppCapability [out]

Capability value. The <b>BSTR</b> is allocated using 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>
 

 

