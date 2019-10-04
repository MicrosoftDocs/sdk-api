---
UID: NS:clusapi.CLUSPROP_DWORD
title: CLUSPROP_DWORD (clusapi.h)
author: windows-sdk-content
description: Describes a numeric value identifying the physical drive of a disk.
old-location: mscs\clusprop_disk_number.htm
tech.root: MsCS
ms.assetid: 8230d356-0d5a-4859-ae03-c25d078684b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSPROP_DISK_NUMBER, *PCLUSPROP_DISK_SIGNATURE, *PCLUSPROP_DWORD, CLUSPROP_DISK_NUMBER, CLUSPROP_DISK_NUMBER structure [Failover Cluster], CLUSPROP_DISK_SIGNATURE, CLUSPROP_DWORD, PCLUSPROP_DISK_NUMBER, PCLUSPROP_DISK_NUMBER structure pointer [Failover Cluster], _wolf_clusprop_disk_number, clusapi/CLUSPROP_DISK_NUMBER, clusapi/PCLUSPROP_DISK_NUMBER, mscs.clusprop_disk_number"
ms.topic: struct
f1_keywords: 
 - "clusapi/CLUSPROP_DISK_NUMBER"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: CLUSPROP_DWORD, *PCLUSPROP_DWORD
req.redist: 
ms.custom: 19H1
---

# CLUSPROP_DWORD structure


## -description


Describes a 
    numeric value identifying the physical drive of a disk. It is used as an entry in a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>DWORD</b> value identifying the physical drive of a disk.</li>
</ul>For convenience, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field dw

Numeric value identifying the physical drive of the disk. Valid values begin at zero.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_DISK_NUMBER</b> (0x00070002).


#### - cbLength

Member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure 
      indicating the count of bytes in the <b>dw</b> member.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>
 

 

