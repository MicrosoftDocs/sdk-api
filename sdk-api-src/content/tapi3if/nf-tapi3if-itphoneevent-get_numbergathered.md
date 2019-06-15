---
UID: NF:tapi3if.ITPhoneEvent.get_NumberGathered
title: ITPhoneEvent::get_NumberGathered (tapi3if.h)
author: windows-sdk-content
description: The get_NumberGathered method returns a BSTR value specifying the phone number that was gathered. This information is available only when the ITPhoneEvent::get_Event method returns PE_NUMBERGATHERED.
old-location: tapi3\itphoneevent_get_numbergathered.htm
tech.root: Tapi
ms.assetid: 04537dbb-e1a1-445c-963e-13a8733f2566
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_NumberGathered method, ITPhoneEvent.get_NumberGathered, ITPhoneEvent::get_NumberGathered, _tapi3_itphoneevent_get_numbergathered, get_NumberGathered, get_NumberGathered method [TAPI 2.2], get_NumberGathered method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_numbergathered, tapi3if/ITPhoneEvent::get_NumberGathered
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
ms.custom: 19H1
---

# ITPhoneEvent::get_NumberGathered


## -description


The 
<b>get_NumberGathered</b> method returns a <b>BSTR</b> value specifying the phone number that was gathered. This information is available only when the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a> method returns PE_NUMBERGATHERED.


## -parameters




### -param ppNumber [out]

Phone number that was gathered. The <b>BSTR</b> is allocated using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> and should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>
 

 

