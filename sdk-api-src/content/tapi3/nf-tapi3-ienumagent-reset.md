---
UID: NF:tapi3.IEnumAgent.Reset
title: IEnumAgent::Reset (tapi3.h)
author: windows-sdk-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: tapi3\ienumagent_reset.htm
tech.root: Tapi
ms.assetid: e909135a-04ed-4602-991e-915744667df7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumAgent interface [TAPI 2.2],Reset method, IEnumAgent.Reset, IEnumAgent::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumAgent interface, _tapi3_ienumagent_reset, tapi3.ienumagent_reset, tapi3cc/IEnumAgent::Reset
ms.topic: method
f1_keywords: 
 - "tapi3/IEnumAgent.Reset"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumAgent.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAgent::Reset


## -description


The 
<b>Reset</b> method resets the enumeration sequence to the beginning.


## -parameters






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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumagent">IEnumAgent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
 

 

