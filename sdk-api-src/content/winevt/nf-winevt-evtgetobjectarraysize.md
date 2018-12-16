---
UID: NF:winevt.EvtGetObjectArraySize
title: EvtGetObjectArraySize function
author: windows-sdk-content
description: Gets the number of elements in the array of objects.
old-location: wes\evtgetobjectarraysize.htm
tech.root: wes
ms.assetid: fc4043ac-48eb-400b-8cf6-b83cbbb2765c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtGetObjectArraySize, EvtGetObjectArraySize function [EventLog], wes.evtgetobjectarraysize, winevt/EvtGetObjectArraySize
ms.topic: function
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtGetObjectArraySize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtGetObjectArraySize function


## -description


Gets the number of elements in the array of objects.


## -parameters




### -param ObjectArray [in]

A handle to an array of objects that the <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a> function returns.


### -param ObjectArraySize [out]

The number of elements in the array.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a>



<a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a>
 

 

