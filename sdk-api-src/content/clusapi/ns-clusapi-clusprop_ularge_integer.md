---
UID: NS:clusapi.CLUSPROP_ULARGE_INTEGER
title: CLUSPROP_ULARGE_INTEGER
author: windows-sdk-content
description: Describes an unsigned large integer.
old-location: mscs\clusprop_ularge_integer.htm
tech.root: MsCS
ms.assetid: 1db28e46-e5e0-4d99-b9a8-80c3f1534ca6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PCLUSPROP_ULARGE_INTEGER, CLUSPROP_ULARGE_INTEGER, CLUSPROP_ULARGE_INTEGER structure [Failover Cluster], PCLUSPROP_ULARGE_INTEGER, PCLUSPROP_ULARGE_INTEGER structure pointer [Failover Cluster], _wolf_clusprop_ularge_integer, clusapi/CLUSPROP_ULARGE_INTEGER, clusapi/PCLUSPROP_ULARGE_INTEGER, mscs.clusprop_ularge_integer"
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
 - CLUSPROP_ULARGE_INTEGER
product: Windows
targetos: Windows
req.typenames: CLUSPROP_ULARGE_INTEGER
req.redist: 
---

# CLUSPROP_ULARGE_INTEGER structure


## -description


Describes an unsigned large integer. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the integer value.</li>
<li>An unsigned large integer value.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> members are listed 
    explicitly.


## -struct-fields




### -field li

Unsigned large integer value.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_ULARGE_INTEGER</b> (0x00010006).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>li</b> member.


## -remarks



Use caution when referencing large integer values in <b>DWORD</b>-aligned structures such 
     as value lists, <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property lists</a>, and 
     <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0h or 8h. 
     <b>DWORD</b> alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or Ch), which will cause an alignment fault when the data is read or written. You can avoid 
     alignment faults by separately copying the high and low <b>DWORD</b> parts of large values 
     into local variables, which are guaranteed to be naturally aligned.




## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

