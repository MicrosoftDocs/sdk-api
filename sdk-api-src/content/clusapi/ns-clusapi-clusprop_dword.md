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
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>DWORD</b> value identifying the physical drive of a disk.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field dw

Numeric value identifying the physical drive of the disk. Valid values begin at zero.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_DISK_NUMBER</b> (0x00070002).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure 
      indicating the count of bytes in the <b>dw</b> member.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

