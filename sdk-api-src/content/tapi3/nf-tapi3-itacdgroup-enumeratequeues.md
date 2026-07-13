---
UID: NF:tapi3.ITACDGroup.EnumerateQueues
title: ITACDGroup::EnumerateQueues (tapi3.h)
description: The ITACDGroup::EnumerateQueues method (tapi3.h) enumerates queues currently on the ACD group. This method is provided for C and C++ applications.
helpviewer_keywords: ["EnumerateQueues","EnumerateQueues method [TAPI 2.2]","EnumerateQueues method [TAPI 2.2]","ITACDGroup interface","ITACDGroup interface [TAPI 2.2]","EnumerateQueues method","ITACDGroup.EnumerateQueues","ITACDGroup::EnumerateQueues","_tapi3_itacdgroup_enumeratequeues","tapi3.itacdgroup_enumeratequeues","tapi3cc/ITACDGroup::EnumerateQueues"]
old-location: tapi3\itacdgroup_enumeratequeues.htm
tech.root: tapi3
ms.assetid: 1d9e0dcf-ce43-494f-8adc-845d2856bdd1
ms.date: 08/09/2022
ms.keywords: EnumerateQueues, EnumerateQueues method [TAPI 2.2], EnumerateQueues method [TAPI 2.2],ITACDGroup interface, ITACDGroup interface [TAPI 2.2],EnumerateQueues method, ITACDGroup.EnumerateQueues, ITACDGroup::EnumerateQueues, _tapi3_itacdgroup_enumeratequeues, tapi3.itacdgroup_enumeratequeues, tapi3cc/ITACDGroup::EnumerateQueues
req.header: tapi3.h
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
 - ITACDGroup::EnumerateQueues
 - tapi3/ITACDGroup::EnumerateQueues
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
 - ITACDGroup.EnumerateQueues
---

# ITACDGroup::EnumerateQueues


## -description

The 
<b>EnumerateQueues</b> method enumerates queues currently on the ACD group. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-get_queues">get_Queues</a> method.

## -parameters

### -param ppEnumQueue [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumqueue">IEnumQueue</a> interface.

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
The <i>ppEnumQueue</i> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumqueue">IEnumQueue</a> interface returned by <b>ITACDGroup::EnumerateQueues</b>. The application must call <b>Release</b> on the 
<b>IEnumQueue</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumqueue">IEnumQueue</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-get_queues">get_Queues</a>
