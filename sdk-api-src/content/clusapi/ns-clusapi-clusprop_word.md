---
UID: NS:clusapi.CLUSPROP_WORD
title: CLUSPROP_WORD
author: windows-sdk-content
description: Describes numeric data.
old-location: mscs\clusprop_word.htm
old-project: mscs
ms.assetid: ba09290b-171b-45cf-a367-485f7322ebef
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCLUSPROP_WORD, CLUSPROP_WORD, CLUSPROP_WORD structure [Failover Cluster], PCLUSPROP_WORD, PCLUSPROP_WORD structure pointer [Failover Cluster], _wolf_clusprop_word, clusapi/CLUSPROP_WORD, clusapi/PCLUSPROP_WORD, mscs.clusprop_word"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CLUSPROP_WORD, *PCLUSPROP_WORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_WORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSPROP_WORD structure


## -description


Describes numeric data. It 
    is used as an entry in a <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>WORD</b> value.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field w

Numeric value.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure describing 
       the format and type of the <b>w</b> member.


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <b>w</b> member.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

