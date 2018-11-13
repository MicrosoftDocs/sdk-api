---
UID: NS:clusapi.CLUSPROP_ULARGE_INTEGER
title: CLUSPROP_ULARGE_INTEGER
author: windows-sdk-content
description: Describes an unsigned large integer.
old-location: mscs\clusprop_ularge_integer.htm
tech.root: mscs
ms.assetid: 1db28e46-e5e0-4d99-b9a8-80c3f1534ca6
ms.author: windowssdkdev
ms.date: 11/06/2018
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
    <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the integer value.</li>
<li>An unsigned large integer value.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> members are listed 
    explicitly.


## -struct-fields




### -field li

Unsigned large integer value.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_ULARGE_INTEGER</b> (0x00010006).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>li</b> member.


## -remarks



Use caution when referencing large integer values in <b>DWORD</b>-aligned structures such 
     as value lists, <a href="https://msdn.microsoft.com/en-us/library/Aa371809(v=VS.85).aspx">property lists</a>, and 
     <a href="https://msdn.microsoft.com/en-us/library/Aa371782(v=VS.85).aspx">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0h or 8h. 
     <b>DWORD</b> alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or Ch), which will cause an alignment fault when the data is read or written. You can avoid 
     alignment faults by separately copying the high and low <b>DWORD</b> parts of large values 
     into local variables, which are guaranteed to be naturally aligned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>
 

 

