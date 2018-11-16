---
UID: NF:tapi3if.ITPhoneEvent.get_NumberGathered
title: ITPhoneEvent::get_NumberGathered
author: windows-sdk-content
description: The get_NumberGathered method returns a BSTR value specifying the phone number that was gathered. This information is available only when the ITPhoneEvent::get_Event method returns PE_NUMBERGATHERED.
old-location: tapi3\itphoneevent_get_numbergathered.htm
tech.root: Tapi
ms.assetid: 04537dbb-e1a1-445c-963e-13a8733f2566
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_NumberGathered method, ITPhoneEvent.get_NumberGathered, ITPhoneEvent::get_NumberGathered, _tapi3_itphoneevent_get_numbergathered, get_NumberGathered, get_NumberGathered method [TAPI 2.2], get_NumberGathered method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_numbergathered, tapi3if/ITPhoneEvent::get_NumberGathered
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
 - ITPhoneEvent.get_NumberGathered
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
- ITPhoneEvent.get_NumberGathered
: 
---

# ITPhoneEvent::get_NumberGathered


## -description


The 
<b>get_NumberGathered</b> method returns a <b>BSTR</b> value specifying the phone number that was gathered. This information is available only when the 
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a> method returns PE_NUMBERGATHERED.


## -parameters




### -param ppNumber [out]

Phone number that was gathered. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a> and should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>



<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

