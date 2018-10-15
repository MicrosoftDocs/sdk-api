---
UID: NS:clusapi.CLUSPROP_SECURITY_DESCRIPTOR
title: CLUSPROP_SECURITY_DESCRIPTOR
author: windows-sdk-content
description: Describes a security descriptor.
old-location: mscs\clusprop_security_descriptor.htm
tech.root: mscs
ms.assetid: b19358cf-1cf9-4d91-85df-ed7fa804a7f2
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*PCLUSPROP_SECURITY_DESCRIPTOR, CLUSPROP_SECURITY_DESCRIPTOR, CLUSPROP_SECURITY_DESCRIPTOR structure [Failover Cluster], PCLUSPROP_SECURITY_DESCRIPTOR, PCLUSPROP_SECURITY_DESCRIPTOR structure pointer [Failover Cluster], _wolf_clusprop_security_descriptor, clusapi/CLUSPROP_SECURITY_DESCRIPTOR, clusapi/PCLUSPROP_SECURITY_DESCRIPTOR, mscs.clusprop_security_descriptor"
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
 - CLUSPROP_SECURITY_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: CLUSPROP_SECURITY_DESCRIPTOR, *PCLUSPROP_SECURITY_DESCRIPTOR
req.redist: 
---

# CLUSPROP_SECURITY_DESCRIPTOR structure


## -description


Describes a security descriptor. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A security descriptor in 
     <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">self-relative</a> 
     format.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> members are listed 
    explicitly.


## -struct-fields




### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.sd

Security descriptor in 
       <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">self-relative</a> format. 
       For more information about self-relative security descriptors, see 
       <a href="https://msdn.microsoft.com/en-us/library/Aa374807(v=VS.85).aspx">Absolute and Self-Relative Security Descriptors</a>.


### -field DUMMYUNIONNAME.rgbSecurityDescriptor

Byte array to address the entire security descriptor including the owner, group, SACL, and DACL fields (if 
       present) that follow the <b>SECURITY_DESCRIPTOR_RELATIVE</b> structure.


### -field CLUSPROP_VALUE

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure with a 
      value of <b>CLUSPROP_SYNTAX_LIST_VALUE_SECURITY_DESCRIPTOR</b> (0x00010009).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
      the count of bytes in the security descriptor that follows the 
      <b>CLUSPROP_VALUE</b> header. Padding bytes are not included 
      in the count.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data Structures</a>
 

 

