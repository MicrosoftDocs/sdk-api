---
UID: NS:clusapi.CLUSPROP_VALUE
title: CLUSPROP_VALUE
author: windows-sdk-content
description: Describes the syntax and length of a data value used in a value list. The CLUSPROP_VALUE structure is used as a generic header in all of the structures that describe data of a particular type, such as CLUSPROP_BINARY and CLUSPROP_SZ.
old-location: mscs\clusprop_value.htm
tech.root: mscs
ms.assetid: a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUSPROP_VALUE, CLUSPROP_VALUE, CLUSPROP_VALUE structure [Failover Cluster], PCLUSPROP_VALUE, PCLUSPROP_VALUE structure pointer [Failover Cluster], _wolf_clusprop_value, clusapi/CLUSPROP_VALUE, clusapi/PCLUSPROP_VALUE, mscs.clusprop_value"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CLUSPROP_VALUE
product: Windows
targetos: Windows
req.typenames: CLUSPROP_VALUE, *PCLUSPROP_VALUE
req.redist: 
---

# CLUSPROP_VALUE structure


## -description


Describes the syntax and 
    length of a data value used in a <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a>. The 
    <b>CLUSPROP_VALUE</b> structure is used as a generic header in 
    all of the structures that describe data of a particular type, such as 
    <a href="https://msdn.microsoft.com/en-us/library/Aa368368(v=VS.85).aspx">CLUSPROP_BINARY</a> and 
    <a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>.


## -struct-fields




### -field Syntax


<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a> union that describes a 
      value.


### -field cbLength

Count of bytes in the data that follows this 
      <b>CLUSPROP_VALUE</b> structure.


## -remarks



The <b>CLUSPROP_VALUE</b> structure is used to describe the 
     format, type, and length of a data value in the following structures:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368368(v=VS.85).aspx">CLUSPROP_BINARY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368373(v=VS.85).aspx">CLUSPROP_DISK_NUMBER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/38400cce-d84a-4439-9dab-20102c1580ff">CLUSPROP_DISK_SIGNATURE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309110(v=VS.85).aspx">CLUSPROP_FILETIME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368379(v=VS.85).aspx">CLUSPROP_LONG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368380(v=VS.85).aspx">CLUSPROP_MULTI_SZ</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368381(v=VS.85).aspx">CLUSPROP_PARTITION_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309113(v=VS.85).aspx">CLUSPROP_PARTITION_INFO_EX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368384(v=VS.85).aspx">CLUSPROP_REQUIRED_DEPENDENCY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368385(v=VS.85).aspx">CLUSPROP_RESOURCE_CLASS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368386(v=VS.85).aspx">CLUSPROP_RESOURCE_CLASS_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368387(v=VS.85).aspx">CLUSPROP_SCSI_ADDRESS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368392(v=VS.85).aspx">CLUSPROP_ULARGE_INTEGER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa368394(v=VS.85).aspx">CLUSPROP_WORD</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368368(v=VS.85).aspx">CLUSPROP_BINARY</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

