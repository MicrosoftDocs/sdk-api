---
UID: NF:tapi3.IEnumACDGroup.Skip
title: IEnumACDGroup::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumacdgroup_skip.htm
old-project: Tapi
ms.assetid: 58f794cc-da10-4772-9afe-078337b7734b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEnumACDGroup interface [TAPI 2.2],Skip method, IEnumACDGroup.Skip, IEnumACDGroup::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumACDGroup interface, _tapi3_ienumacdgroup_skip, tapi3.ienumacdgroup_skip, tapi3cc/IEnumACDGroup::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumACDGroup.Skip
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumACDGroup::Skip


## -description


The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

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




<a href="https://msdn.microsoft.com/301cd27e-00ac-44a4-b5c6-0efcb36ad974">IEnumACDGroup</a>



<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>
 

 

