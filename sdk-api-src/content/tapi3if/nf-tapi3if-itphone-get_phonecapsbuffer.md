---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

