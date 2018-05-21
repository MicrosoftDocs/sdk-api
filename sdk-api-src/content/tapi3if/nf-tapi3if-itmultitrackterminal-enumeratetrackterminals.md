---
UID: NF:tapi3if.ITMultiTrackTerminal.EnumerateTrackTerminals
title: ITMultiTrackTerminal::EnumerateTrackTerminals
author: windows-driver-content
description: The EnumerateTrackTerminals method creates and returns an enumeration containing the terminals contained by the multitrack terminal on which this method was called.
old-location: tapi3\itmultitrackterminal_enumeratetrackterminals.htm
old-project: Tapi
ms.assetid: 90ef12f5-1a94-49ca-85c3-092306503827
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: EnumerateTrackTerminals, EnumerateTrackTerminals method [TAPI 2.2], EnumerateTrackTerminals method [TAPI 2.2],ITMultiTrackTerminal interface, ITMultiTrackTerminal interface [TAPI 2.2],EnumerateTrackTerminals method, ITMultiTrackTerminal.EnumerateTrackTerminals, ITMultiTrackTerminal::EnumerateTrackTerminals, _tapi3_itmultitrackterminal_enumeratetrackterminals, tapi3.itmultitrackterminal_enumeratetrackterminals, tapi3if/ITMultiTrackTerminal::EnumerateTrackTerminals
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITMultiTrackTerminal.EnumerateTrackTerminals
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMultiTrackTerminal::EnumerateTrackTerminals


## -description


The 
<b>EnumerateTrackTerminals</b> method creates and returns an enumeration containing the terminals contained by the multitrack terminal on which this method was called.


## -parameters




### -param ppEnumTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface enumerating terminals contained in the multitrack terminal.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminalEnum</i> parameter is not a valid pointer.

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
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface returned by <b>ITMultiTrackTerminal::EnumerateTrackTerminals</b>. The application must call <b>Release</b> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a>



<a href="https://msdn.microsoft.com/c9e5d8a4-78a6-4449-9c11-c780e72ab925">ITMultiTrackTerminal</a>
 

 

