---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# EngQuerySystemAttribute function


## -description


The <b>EngQuerySystemAttribute</b> function queries processor-specific or system-specific capabilities.


## -parameters




### -param CapNum [in]

Specifies the capability being queried. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>EngNumberOfProcessors</b>

</td>
<td>
GDI returns the number of active processors in the system.

</td>
</tr>
<tr>
<td>
<b>EngOptimumAvailableSystemMemory</b>

</td>
<td>
Not available for use.

</td>
</tr>
<tr>
<td>
<b>EngOptimumAvailableUserMemory</b>

</td>
<td>
Not available for use.

</td>
</tr>
<tr>
<td>
<b>EngProcessorFeature</b>

</td>
<td>
GDI returns a bitmask of flags that describe the features of the processor. Currently, GDI sets the QSA_MMX flag when an <i>x86</i> processor has MMX support. QSA_MMX is relevant only on the <i>x86</i> platform.

</td>
</tr>
</table>
 


### -param pCapability [out]

Pointer to the location that receives the result of the query. The value that GDI places in this parameter depends on the enumerated value specified by <i>CapNum</i>.


## -returns



<b>EngQuerySystemAttribute</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.



