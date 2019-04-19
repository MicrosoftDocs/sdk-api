---
UID: NS:clusapi.CLUSPROP_SZ
title: CLUSPROP_SZ (clusapi.h)
author: windows-sdk-content
description: Describes multiple NULL-terminated Unicode strings.
old-location: mscs\clusprop_multi_sz.htm
tech.root: MsCS
ms.assetid: 3c508ed6-eec8-4fa9-9ae7-9c8d7f4c8b98
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSPROP_MULTI_SZ, *PCLUSPROP_PROPERTY_NAME, *PCLUSPROP_SZ, CLUSPROP_MULTI_SZ, CLUSPROP_MULTI_SZ structure [Failover Cluster], CLUSPROP_PROPERTY_NAME, CLUSPROP_SZ, PCLUSPROP_MULTI_SZ, PCLUSPROP_MULTI_SZ structure pointer [Failover Cluster], _wolf_clusprop_multi_sz, clusapi/CLUSPROP_MULTI_SZ, clusapi/PCLUSPROP_MULTI_SZ, mscs.clusprop_multi_sz"
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
 - CLUSPROP_MULTI_SZ
product: Windows
targetos: Windows
req.typenames: CLUSPROP_SZ, *PCLUSPROP_SZ
req.redist: 
ms.custom: 19H1
---

# CLUSPROP_SZ structure


## -description


Describes multiple 
    <b>NULL</b>-terminated Unicode strings. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A string array.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field sz

Multiple null-terminated Unicode strings with the last string followed by an additional 
       <b>NULL</b>-terminating character.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_MULTI_SZ</b> (0x00010005).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>sz</b> member. Padding bytes are not included in the 
       count.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

