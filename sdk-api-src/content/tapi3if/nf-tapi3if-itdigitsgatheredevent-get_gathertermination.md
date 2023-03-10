---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_GatherTermination
title: ITDigitsGatheredEvent::get_GatherTermination (tapi3if.h)
description: The get_GatherTermination method gets the reason why the TAPI Server terminated the gathering of digits on the call.
helpviewer_keywords: ["ITDigitsGatheredEvent interface [TAPI 2.2]","get_GatherTermination method","ITDigitsGatheredEvent.get_GatherTermination","ITDigitsGatheredEvent::get_GatherTermination","_tapi3_itdigitsgatheredevent_get_gathertermination","get_GatherTermination","get_GatherTermination method [TAPI 2.2]","get_GatherTermination method [TAPI 2.2]","ITDigitsGatheredEvent interface","tapi3.itdigitsgatheredevent_get_gathertermination","tapi3if/ITDigitsGatheredEvent::get_GatherTermination"]
old-location: tapi3\itdigitsgatheredevent_get_gathertermination.htm
tech.root: tapi3
ms.assetid: 97c123b9-4497-43f3-b747-660d3f9f5848
ms.date: 12/05/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_GatherTermination method, ITDigitsGatheredEvent.get_GatherTermination, ITDigitsGatheredEvent::get_GatherTermination, _tapi3_itdigitsgatheredevent_get_gathertermination, get_GatherTermination, get_GatherTermination method [TAPI 2.2], get_GatherTermination method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_gathertermination, tapi3if/ITDigitsGatheredEvent::get_GatherTermination
req.header: tapi3if.h
req.include-header: 
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
 - ITDigitsGatheredEvent::get_GatherTermination
 - tapi3if/ITDigitsGatheredEvent::get_GatherTermination
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
 - ITDigitsGatheredEvent.get_GatherTermination
---

# ITDigitsGatheredEvent::get_GatherTermination


## -description

The 
<b>get_GatherTermination</b> method gets the reason why the TAPI Server terminated the gathering of digits on the call.

## -parameters

### -param pGatherTermination [out]

Pointer to a value from the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_gatherterm">TAPI_GATHERTERM</a> enumeration.

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
The <i>pGatherTermination</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitsgatheredevent">ITDigitsGatheredEvent</a>