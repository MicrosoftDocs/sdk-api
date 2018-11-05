---
UID: NS:clusapi.CLUSPROP_LARGE_INTEGER
title: CLUSPROP_LARGE_INTEGER
author: windows-sdk-content
description: Describes a signed large integer.
old-location: mscs\clusprop_large_integer.htm
tech.root: mscs
ms.assetid: 3e0849e6-3d93-47cb-858d-9891451b8dfd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PCLUSPROP_LARGE_INTEGER, CLUSPROP_LARGE_INTEGER, CLUSPROP_LARGE_INTEGER structure [Failover Cluster], PCLUSPROP_LARGE_INTEGER, PCLUSPROP_LARGE_INTEGER structure pointer [Failover Cluster], _wolf_clusprop_large_integer, clusapi/CLUSPROP_LARGE_INTEGER, clusapi/PCLUSPROP_LARGE_INTEGER, mscs.clusprop_large_integer"
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
    a signed large integer. It is used as an entry in a <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a> 
    and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the integer value.</li>
<li>Assigned large integer value.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> members are listed 
    explicitly.


## -struct-fields




### -field li

Signed large integer value.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure describing 
       the format and type of the unsigned large integer.


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>li</b> member.


## -remarks



Use caution when referencing large integer values in <b>DWORD</b>-aligned structures such 
     as value lists, <a href="https://msdn.microsoft.com/en-us/library/Aa371809(v=VS.85).aspx">property lists</a>, and 
     <a href="https://msdn.microsoft.com/en-us/library/Aa371782(v=VS.85).aspx">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0h or 8h. 
     <b>DWORD</b>-alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or Ch), which will cause an alignment fault when the data is read or written. You can avoid 
     alignment faults by separately copying the high and low <b>DWORD</b>s of large values into 
     local variables, which are guaranteed to be naturally aligned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383713(v=VS.85).aspx">LARGE_INTEGER</a>
 

 

