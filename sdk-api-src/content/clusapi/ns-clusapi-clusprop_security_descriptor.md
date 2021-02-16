---
UID: NS:clusapi.CLUSPROP_SECURITY_DESCRIPTOR
title: CLUSPROP_SECURITY_DESCRIPTOR (clusapi.h)
description: Describes a security descriptor.
helpviewer_keywords: ["*PCLUSPROP_SECURITY_DESCRIPTOR","CLUSPROP_SECURITY_DESCRIPTOR","CLUSPROP_SECURITY_DESCRIPTOR structure [Failover Cluster]","PCLUSPROP_SECURITY_DESCRIPTOR","PCLUSPROP_SECURITY_DESCRIPTOR structure pointer [Failover Cluster]","_wolf_clusprop_security_descriptor","clusapi/CLUSPROP_SECURITY_DESCRIPTOR","clusapi/PCLUSPROP_SECURITY_DESCRIPTOR","mscs.clusprop_security_descriptor"]
old-location: mscs\clusprop_security_descriptor.htm
tech.root: MsCS
ms.assetid: b19358cf-1cf9-4d91-85df-ed7fa804a7f2
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_SECURITY_DESCRIPTOR, CLUSPROP_SECURITY_DESCRIPTOR, CLUSPROP_SECURITY_DESCRIPTOR structure [Failover Cluster], PCLUSPROP_SECURITY_DESCRIPTOR, PCLUSPROP_SECURITY_DESCRIPTOR structure pointer [Failover Cluster], _wolf_clusprop_security_descriptor, clusapi/CLUSPROP_SECURITY_DESCRIPTOR, clusapi/PCLUSPROP_SECURITY_DESCRIPTOR, mscs.clusprop_security_descriptor'
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
targetos: Windows
req.typenames: CLUSPROP_SECURITY_DESCRIPTOR, *PCLUSPROP_SECURITY_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_SECURITY_DESCRIPTOR
 - clusapi/CLUSPROP_SECURITY_DESCRIPTOR
 - PCLUSPROP_SECURITY_DESCRIPTOR
 - clusapi/PCLUSPROP_SECURITY_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_SECURITY_DESCRIPTOR
---

# CLUSPROP_SECURITY_DESCRIPTOR structure


## -description

Describes a security descriptor. It is used as an entry in a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A security descriptor in 
     <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> 
     format.</li>
</ul>

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.sd

Security descriptor in 
       <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> format. 
       For more information about self-relative security descriptors, see 
       <a href="/windows/desktop/SecAuthZ/absolute-and-self-relative-security-descriptors">Absolute and Self-Relative Security Descriptors</a>.

### -field DUMMYUNIONNAME.rgbSecurityDescriptor

Byte array to address the entire security descriptor including the owner, group, SACL, and DACL fields (if 
       present) that follow the <b>SECURITY_DESCRIPTOR_RELATIVE</b> structure.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_SECURITY_DESCRIPTOR</b> (0x00010009) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>DUMMYUNIONNAME</b> member. Padding bytes are not included in the count.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>