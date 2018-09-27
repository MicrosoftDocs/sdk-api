---
UID: NF:tapi3if.ITPhone.get_PhoneCapsBuffer
title: ITPhone::get_PhoneCapsBuffer
author: windows-sdk-content
description: The get_PhoneCapsBuffer method gets a buffer capability/information about the phone, based on the PHONECAPS_BUFFER enum passed in.
old-location: tapi3\itphone_get_phonecapsbuffer.htm
tech.root: tapi
ms.assetid: d9397aa8-2be4-4775-8123-975bdd58a6b5
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PhoneCapsBuffer method, ITPhone.get_PhoneCapsBuffer, ITPhone::get_PhoneCapsBuffer, _tapi3_itphone_get_phonecapsbuffer, get_PhoneCapsBuffer, get_PhoneCapsBuffer method [TAPI 2.2], get_PhoneCapsBuffer method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_phonecapsbuffer, tapi3if/ITPhone::get_PhoneCapsBuffer
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
 - ITPhone.get_PhoneCapsBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_PhoneCapsBuffer


## -description


The 
<b>get_PhoneCapsBuffer</b> method gets a buffer capability/information about the phone, based on the 
<a href="https://msdn.microsoft.com/208efd60-58b2-4d0a-b757-29b1db017195">PHONECAPS_BUFFER</a> enum passed in.

This method is intended for Visual Basic and scripting applications. C/C++ applications must use the 
<a href="https://msdn.microsoft.com/239902ca-0e9e-4b8d-927d-ee46a35dd9d8">GetPhoneCapsBuffer</a> method.


## -parameters




### -param pcbCaps [in]

The 
<a href="https://msdn.microsoft.com/208efd60-58b2-4d0a-b757-29b1db017195">PHONECAPS_BUFFER</a> descriptor for the phone capability.


### -param pVarBuffer [out]

Pointer to VARIANT containing the capability value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>
 

 

