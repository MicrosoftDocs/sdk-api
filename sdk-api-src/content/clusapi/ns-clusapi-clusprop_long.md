---
UID: NS:clusapi.CLUSPROP_LONG
title: CLUSPROP_LONG
author: windows-sdk-content
description: Describes signed LONG data.
old-location: mscs\clusprop_long.htm
tech.root: mscs
ms.assetid: aa214e43-cadc-4f06-8c98-e6a5b13258b8
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCLUSPROP_LONG, CLUSPROP_LONG, CLUSPROP_LONG structure [Failover Cluster], PCLUSPROP_LONG, PCLUSPROP_LONG structure pointer [Failover Cluster], _wolf_clusprop_long, clusapi/CLUSPROP_LONG, clusapi/PCLUSPROP_LONG, mscs.clusprop_long"
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
    <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>LONG</b> value.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field l

Signed <b>LONG</b> value.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_LONG</b> (0x00010007).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>l</b> member.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>
 

 

