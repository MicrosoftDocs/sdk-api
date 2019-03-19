---
UID: NS:clusapi.CLUSPROP_LONG
title: CLUSPROP_LONG (clusapi.h)
author: windows-sdk-content
description: Describes signed LONG data.
old-location: mscs\clusprop_long.htm
tech.root: MsCS
ms.assetid: aa214e43-cadc-4f06-8c98-e6a5b13258b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUSPROP_LONG, CLUSPROP_LONG, CLUSPROP_LONG structure [Failover Cluster], PCLUSPROP_LONG, PCLUSPROP_LONG structure pointer [Failover Cluster], _wolf_clusprop_long, clusapi/CLUSPROP_LONG, clusapi/PCLUSPROP_LONG, mscs.clusprop_long"
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusAPI.h
api_name:
 - CLUSPROP_LONG
product: Windows
targetos: Windows
req.typenames: CLUSPROP_LONG, *PCLUSPROP_LONG
req.redist: 
---

# CLUSPROP_LONG structure


## -description


Describes signed 
    <b>LONG</b> data. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>LONG</b> value.</li>
</ul>

## -struct-fields




### -field l

Signed <b>LONG</b> value.


### -field CLUSPROP_VALUE


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_LONG</b> (0x00010007) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>l</b> member.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

