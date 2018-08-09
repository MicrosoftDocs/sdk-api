---
UID: NF:tapi3if.ITPhone.GetPhoneCapsBuffer
title: ITPhone::GetPhoneCapsBuffer
author: windows-sdk-content
description: The GetPhoneCapsBuffer method gets a buffer capability/information about the phone, based on the PHONECAPS_BUFFER enum passed in.
old-location: tapi3\itphone_getphonecapsbuffer.htm
old-project: tapi
ms.assetid: 239902ca-0e9e-4b8d-927d-ee46a35dd9d8
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: GetPhoneCapsBuffer, GetPhoneCapsBuffer method [TAPI 2.2], GetPhoneCapsBuffer method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],GetPhoneCapsBuffer method, ITPhone.GetPhoneCapsBuffer, ITPhone::GetPhoneCapsBuffer, _tapi3_itphone_getphonecapsbuffer, tapi3.itphone_getphonecapsbuffer, tapi3if/ITPhone::GetPhoneCapsBuffer
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
 - ITPhone.GetPhoneCapsBuffer
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::GetPhoneCapsBuffer


## -description


The 
<b>GetPhoneCapsBuffer</b> method gets a buffer capability/information about the phone, based on the 
<a href="https://msdn.microsoft.com/208efd60-58b2-4d0a-b757-29b1db017195">PHONECAPS_BUFFER</a> enum passed in.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/d9397aa8-2be4-4775-8123-975bdd58a6b5">get_PhoneCapsBuffer</a> method.


## -parameters




### -param pcbCaps [in]

The 
<a href="https://msdn.microsoft.com/208efd60-58b2-4d0a-b757-29b1db017195">PHONECAPS_BUFFER</a> descriptor for the phone capability.


### -param pdwSize [out]

Size of the buffer, in bytes.


### -param ppPhoneCapsBuffer [out]

Pointer to the buffer containing the values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>
 

 

