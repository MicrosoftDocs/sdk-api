---
UID: NF:tapi3cc.ITACDGroup.get_Queues
title: ITACDGroup::get_Queues (tapi3cc.h)
description: The ITACDGroup::get_Queues method (tapi3cc.h) creates a collection of queues associated with the current ACD group.
helpviewer_keywords: ["ITACDGroup interface [TAPI 2.2]","get_Queues method","ITACDGroup.get_Queues","ITACDGroup::get_Queues","_tapi3_itacdgroup_get_queues","get_Queues","get_Queues method [TAPI 2.2]","get_Queues method [TAPI 2.2]","ITACDGroup interface","tapi3.itacdgroup_get_queues","tapi3cc/ITACDGroup::get_Queues"]
old-location: tapi3\itacdgroup_get_queues.htm
tech.root: tapi3
ms.assetid: f285fea5-4c08-4d30-8378-0b0aeeea8226
ms.date: 08/10/2022
ms.keywords: ITACDGroup interface [TAPI 2.2],get_Queues method, ITACDGroup.get_Queues, ITACDGroup::get_Queues, _tapi3_itacdgroup_get_queues, get_Queues, get_Queues method [TAPI 2.2], get_Queues method [TAPI 2.2],ITACDGroup interface, tapi3.itacdgroup_get_queues, tapi3cc/ITACDGroup::get_Queues
req.header: tapi3cc.h
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
 - ITACDGroup::get_Queues
 - tapi3cc/ITACDGroup::get_Queues
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
 - ITACDGroup.get_Queues
---

# ITACDGroup::get_Queues


## -description

The 
<b>get_Queues</b> method creates a collection of queues associated with the current ACD group. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-enumeratequeues">EnumerateQueues</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a> interface pointers (queue objects).

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a> interface returned by <b>ITACDGroup::get_Queues</b>. The application must call <b>Release</b> on the 
<b>ITQueue</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-enumeratequeues">EnumerateQueues</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>
