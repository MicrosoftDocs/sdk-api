---
UID: NS:clusapi.CLUSPROP_DWORD
title: CLUSPROP_DWORD
author: windows-sdk-content
description: Describes a numeric value identifying the physical drive of a disk.
old-location: mscs\clusprop_disk_number.htm
tech.root: mscs
ms.assetid: 8230d356-0d5a-4859-ae03-c25d078684b3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCLUSPROP_DISK_NUMBER, *PCLUSPROP_DISK_SIGNATURE, *PCLUSPROP_DWORD, CLUSPROP_DISK_NUMBER, CLUSPROP_DISK_NUMBER structure [Failover Cluster], CLUSPROP_DISK_SIGNATURE, CLUSPROP_DWORD, PCLUSPROP_DISK_NUMBER, PCLUSPROP_DISK_NUMBER structure pointer [Failover Cluster], _wolf_clusprop_disk_number, clusapi/CLUSPROP_DISK_NUMBER, clusapi/PCLUSPROP_DISK_NUMBER, mscs.clusprop_disk_number"
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
 - CLUSPROP_DISK_NUMBER
product: Windows
targetos: Windows
req.typenames: CLUSPROP_DWORD, *PCLUSPROP_DWORD
req.redist: 
---

# CLUSPROP_DWORD structure


## -description


Describes a 
    numeric value identifying the physical drive of a disk. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>DWORD</b> value identifying the physical drive of a disk.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field dw

Numeric value identifying the physical drive of the disk. Valid values begin at zero.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_DISK_NUMBER</b> (0x00070002).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure 
      indicating the count of bytes in the <b>dw</b> member.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>
 

 

