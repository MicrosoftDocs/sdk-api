---
UID: NF:tapi3if.ITPhoneEvent.get_ButtonLampId
title: ITPhoneEvent::get_ButtonLampId
author: windows-sdk-content
description: The get_ButtonLampId method returns a long value indicating which button or lamp triggered the event. This information is available only when ITPhoneEvent::get_Event returns PE_LAMPMODE or PE_BUTTON.
old-location: tapi3\itphoneevent_get_buttonlampid.htm
old-project: tapi
ms.assetid: 43b87d10-8cb9-4795-8778-70c8f8ae6300
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_ButtonLampId method, ITPhoneEvent.get_ButtonLampId, ITPhoneEvent::get_ButtonLampId, _tapi3_itphoneevent_get_buttonlampid, get_ButtonLampId, get_ButtonLampId method [TAPI 2.2], get_ButtonLampId method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_buttonlampid, tapi3if/ITPhoneEvent::get_ButtonLampId
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
 - ITPhoneEvent.get_ButtonLampId
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneEvent::get_ButtonLampId


## -description


The 
<b>get_ButtonLampId</b> method returns a long value indicating which button or lamp triggered the event. This information is available only when 
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a> returns PE_LAMPMODE or PE_BUTTON.


## -parameters




### -param plButtonLampId [out]

Button or lamp ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>



<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

