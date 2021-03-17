---
UID: NF:tapi3if.ITRequestEvent.get_RegistrationInstance
title: ITRequestEvent::get_RegistrationInstance (tapi3if.h)
description: The get_RegistrationInstance method gets the registration instance.
helpviewer_keywords: ["ITRequestEvent interface [TAPI 2.2]","get_RegistrationInstance method","ITRequestEvent.get_RegistrationInstance","ITRequestEvent::get_RegistrationInstance","_tapi3_itrequestevent_get_registrationinstance","get_RegistrationInstance","get_RegistrationInstance method [TAPI 2.2]","get_RegistrationInstance method [TAPI 2.2]","ITRequestEvent interface","tapi3.itrequestevent_get_registrationinstance","tapi3if/ITRequestEvent::get_RegistrationInstance"]
old-location: tapi3\itrequestevent_get_registrationinstance.htm
tech.root: tapi3
ms.assetid: 2fa157f8-fb4d-4163-b496-15bc28cca46b
ms.date: 12/05/2018
ms.keywords: ITRequestEvent interface [TAPI 2.2],get_RegistrationInstance method, ITRequestEvent.get_RegistrationInstance, ITRequestEvent::get_RegistrationInstance, _tapi3_itrequestevent_get_registrationinstance, get_RegistrationInstance, get_RegistrationInstance method [TAPI 2.2], get_RegistrationInstance method [TAPI 2.2],ITRequestEvent interface, tapi3.itrequestevent_get_registrationinstance, tapi3if/ITRequestEvent::get_RegistrationInstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITRequestEvent::get_RegistrationInstance
 - tapi3if/ITRequestEvent::get_RegistrationInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITRequestEvent.get_RegistrationInstance
---

# ITRequestEvent::get_RegistrationInstance


## -description

The 
<b>get_RegistrationInstance</b> method gets the registration instance.

## -parameters

### -param plRegistrationInstance [out]

Pointer to the registration instance.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plRegistrationInstance</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequestevent">ITRequestEvent</a>