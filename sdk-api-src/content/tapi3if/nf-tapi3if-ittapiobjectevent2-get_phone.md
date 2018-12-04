---
UID: NF:tapi3if.ITTAPIObjectEvent2.get_Phone
title: ITTAPIObjectEvent2::get_Phone
author: windows-sdk-content
description: The get_Phone method returns a pointer to the ITPhone interface on the phone object that caused this TAPI object event to be fired.
old-location: tapi3\ittapiobjectevent2_get_phone.htm
tech.root: tapi
ms.assetid: 76e316f6-536b-4531-a4a6-397e258678cc
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITTAPIObjectEvent2 interface [TAPI 2.2],get_Phone method, ITTAPIObjectEvent2.get_Phone, ITTAPIObjectEvent2::get_Phone, _tapi3_ittapiobjectevent2_get_phone, get_Phone, get_Phone method [TAPI 2.2], get_Phone method [TAPI 2.2],ITTAPIObjectEvent2 interface, tapi3.ittapiobjectevent2_get_phone, tapi3if/ITTAPIObjectEvent2::get_Phone
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
 - ITTAPIObjectEvent2.get_Phone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPIObjectEvent2::get_Phone


## -description


The 
<b>get_Phone</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface on the phone object that caused this TAPI object event to be fired.


## -parameters




### -param ppPhone [out]

Pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface returned by <b>ITTAPIObjectEvent2::get_Phone</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/ad4fc838-5a6c-4942-b5a0-ed00cea11ba8">ITTAPIObjectEvent2</a>
 

 

