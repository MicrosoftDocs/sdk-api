---
UID: NS:processthreadsapi._PROCESS_MEMORY_EXHAUSTION_INFO
title: "_PROCESS_MEMORY_EXHAUSTION_INFO"
author: windows-sdk-content
description: Allows applications to configure a process to terminate if an allocation fails to commit memory. This structure is used by the PROCESS_INFORMATION_CLASS class.
old-location: base\process_memory_exhaustion_info.htm
tech.root: procthread
ms.assetid: 5BD60CA2-1F97-4B62-8DD1-D21724186323
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PPROCESS_MEMORY_EXHAUSTION_INFO, PPROCESS_MEMORY_EXHAUSTION_INFO, PPROCESS_MEMORY_EXHAUSTION_INFO structure pointer, PROCESS_MEMORY_EXHAUSTION_INFO, PROCESS_MEMORY_EXHAUSTION_INFO structure, _PROCESS_MEMORY_EXHAUSTION_INFO, base.process_memory_exhaustion_info, processthreadsapi/PPROCESS_MEMORY_EXHAUSTION_INFO, processthreadsapi/PROCESS_MEMORY_EXHAUSTION_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1511 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - PROCESS_MEMORY_EXHAUSTION_INFO
product: Windows
targetos: Windows
req.typenames: PROCESS_MEMORY_EXHAUSTION_INFO, *PPROCESS_MEMORY_EXHAUSTION_INFO
req.redist: 
---

# _PROCESS_MEMORY_EXHAUSTION_INFO structure


## -description


Allows applications to configure a process to terminate if an allocation fails to commit memory. This structure is used by the <a href="https://msdn.microsoft.com/4A09E341-82FB-4E50-B2DD-EEDE443F3F1E">PROCESS_INFORMATION_CLASS</a> class.


## -struct-fields




### -field Version

Version should be set to <b>PME_CURRENT_VERSION</b>.


### -field Reserved

Reserved.


### -field Type

Type of failure.

Type should be set to <b>PMETypeFailFastOnCommitFailure</b> (this is the only type available). 



### -field Value

Used to turn the feature on or off.

<table>
<tr>
<td>Function</td>
<td> Setting</td>
</tr>
<tr>
<td>Enable</td>
<td>PME_FAILFAST_ON_COMMIT_FAIL_ENABLE 
</td>
</tr>
<tr>
<td>Disable</td>
<td>PME_FAILFAST_ON_COMMIT_FAIL_DISABLE 
</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/4A09E341-82FB-4E50-B2DD-EEDE443F3F1E">PROCESS_INFORMATION_CLASS </a>



<a href="https://msdn.microsoft.com/0A5B6B4D-B2FF-4873-85E0-3CCB3EA3BF91">PROCESS_MEMORY_EXHAUSTION_TYPE</a>
 

 

