---
UID: NS:clusapi.CLUSPROP_FILETIME
title: CLUSPROP_FILETIME
author: windows-sdk-content
description: Describes a date and time stamp for a file.
old-location: mscs\clusprop_filetime.htm
old-project: mscs
ms.assetid: 2c88e9db-f218-4b88-9bb0-607fd09e8d0b
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PCLUSPROP_FILETIME, CLUSPROP_FILETIME, CLUSPROP_FILETIME structure [Failover Cluster], PCLUSPROP_FILETIME, PCLUSPROP_FILETIME structure pointer [Failover Cluster], clusapi/CLUSPROP_FILETIME, clusapi/PCLUSPROP_FILETIME, mscs.clusprop_filetime"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUSPROP_FILETIME, *PCLUSPROP_FILETIME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_FILETIME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSPROP_FILETIME structure


## -description


Describes a date 
     and time stamp for a file. It is used as an entry in a 
     <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating the format 
      and type of the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> value.</li>
<li>A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> value.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> members are listed 
     explicitly.


## -struct-fields




### -field ft

A date and time value.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_FILETIME</b> (0x0001000c).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>ft</b> member.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>
 

 

