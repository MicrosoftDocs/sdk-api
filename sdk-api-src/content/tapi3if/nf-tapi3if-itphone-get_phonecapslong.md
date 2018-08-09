---
UID: NF:tapi3if.ITPhone.get_PhoneCapsLong
title: ITPhone::get_PhoneCapsLong
author: windows-sdk-content
description: The get_PhoneCapsLong method gets a DWORD capability of the phone, based on the PHONECAPS_LONG enum passed in. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_get_phonecapslong.htm
old-project: tapi
ms.assetid: 9d7804a7-616b-4efc-9f3b-6d7b1fda1bf6
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PhoneCapsLong method, ITPhone.get_PhoneCapsLong, ITPhone::get_PhoneCapsLong, _tapi3_itphone_get_phonecapslong, get_PhoneCapsLong, get_PhoneCapsLong method [TAPI 2.2], get_PhoneCapsLong method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_phonecapslong, tapi3if/ITPhone::get_PhoneCapsLong
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhone.get_PhoneCapsLong
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::get_PhoneCapsLong


## -description


The 
<b>get_PhoneCapsLong</b> method gets a <b>DWORD</b> capability of the phone, based on the 
<a href="https://msdn.microsoft.com/7a73d5ff-d08a-46e6-b4ad-4f3b973967a7">PHONECAPS_LONG</a> enum passed in. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.


## -parameters




### -param pclCap [in]

The 
<a href="https://msdn.microsoft.com/7a73d5ff-d08a-46e6-b4ad-4f3b973967a7">PHONECAPS_LONG</a> descriptor for the phone capability.


### -param plCapability [out]

Capability value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>
 

 

