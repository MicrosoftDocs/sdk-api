---
UID: NS:clusapi.CLUSPROP_LARGE_INTEGER
title: CLUSPROP_LARGE_INTEGER (clusapi.h)
author: windows-sdk-content
description: Describes a signed large integer.
old-location: mscs\clusprop_large_integer.htm
tech.root: MsCS
ms.assetid: 3e0849e6-3d93-47cb-858d-9891451b8dfd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSPROP_LARGE_INTEGER, CLUSPROP_LARGE_INTEGER, CLUSPROP_LARGE_INTEGER structure [Failover Cluster], PCLUSPROP_LARGE_INTEGER, PCLUSPROP_LARGE_INTEGER structure pointer [Failover Cluster], _wolf_clusprop_large_integer, clusapi/CLUSPROP_LARGE_INTEGER, clusapi/PCLUSPROP_LARGE_INTEGER, mscs.clusprop_large_integer"
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
 - CLUSPROP_LARGE_INTEGER
product: Windows
targetos: Windows
req.typenames: CLUSPROP_LARGE_INTEGER
req.redist: 
---

# CLUSPROP_LARGE_INTEGER structure


## -description


Describes 
    a signed large integer. It is used as an entry in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> 
    and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the integer value.</li>
<li>Assigned large integer value.</li>
</ul>

## -struct-fields




### -field li

Signed large integer value.


### -field CLUSPROP_VALUE


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a  <b>cbLength</b> field indicating 
       the count of bytes in the <b>li</b> member.


## -remarks



Use caution when referencing large integer values in <b>DWORD</b>-aligned structures such 
     as value lists, <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property lists</a>, and 
     <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0h or 8h. 
     <b>DWORD</b>-alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or Ch), which will cause an alignment fault when the data is read or written. You can avoid 
     alignment faults by separately copying the high and low <b>DWORD</b>s of large values into 
     local variables, which are guaranteed to be naturally aligned.




## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>
 

 

