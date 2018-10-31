---
UID: NF:tapi3if.ITTAPI2.get_Phones
title: ITTAPI2::get_Phones
author: windows-sdk-content
description: The get_Phones method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty collection and returns S_OK.
old-location: tapi3\ittapi2_get_phones.htm
tech.root: tapi
ms.assetid: 03fe03fc-c58d-4e2a-a187-5ab9a676e89e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITTAPI2 interface [TAPI 2.2],get_Phones method, ITTAPI2.get_Phones, ITTAPI2::get_Phones, _tapi3_ittapi2_get_phones, get_Phones, get_Phones method [TAPI 2.2], get_Phones method [TAPI 2.2],ITTAPI2 interface, tapi3.ittapi2_get_phones, tapi3if/ITTAPI2::get_Phones
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
 - ITTAPI2.get_Phones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI2::get_Phones


## -description


The 
<b>get_Phones</b> method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty collection and returns S_OK.

This method is intended for Visual Basic and scripting applications. C/C++ applications will find the 
<a href="https://msdn.microsoft.com/6b6aba8d-fbf7-459f-9bc8-79647194b989">EnumeratePhones</a> method more convenient.


## -parameters




### -param pPhones [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface returned by <b>ITTAPI2::get_Phones</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.




## -see-also




<b>IEnumPhone</b>



<a href="https://msdn.microsoft.com/8c67f31e-783e-4371-9f17-063f8ecfc069">ITTAPI2</a>
 

 

