---
UID: NS:clusapi.CLUSPROP_BINARY
title: CLUSPROP_BINARY
author: windows-sdk-content
description: Describes a binary data value.
old-location: mscs\clusprop_binary.htm
tech.root: mscs
ms.assetid: 61169871-4998-4e9f-97dc-77344bbfa962
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCLUSPROP_BINARY, CLUSPROP_BINARY, CLUSPROP_BINARY structure [Failover Cluster], PCLUSPROP_BINARY, PCLUSPROP_BINARY structure pointer [Failover Cluster], _wolf_clusprop_binary, clusapi/CLUSPROP_BINARY, clusapi/PCLUSPROP_BINARY, mscs.clusprop_binary"
ms.prod: windows
ms.technology: windows-sdk
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
 - CLUSPROP_BINARY
product: Windows
targetos: Windows
req.typenames: CLUSPROP_BINARY, *PCLUSPROP_BINARY
req.redist: 
---

# CLUSPROP_BINARY structure


## -description


Describes a binary data value. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_BINARY</b> (0x00010001).</li>
<li>A byte array containing the data.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field rgb

Array of bytes containing the data.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_BINARY</b> (0x00010001).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>rgb</b> member.


## -remarks



Use the <a href="https://msdn.microsoft.com/f4730126-9dbf-438a-a9f2-9e917e5888b8">CLUSPROP_BINARY_DECLARE</a> macro to 
     initialize a <b>CLUSPROP_BINARY</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/f4730126-9dbf-438a-a9f2-9e917e5888b8">CLUSPROP_BINARY_DECLARE</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

