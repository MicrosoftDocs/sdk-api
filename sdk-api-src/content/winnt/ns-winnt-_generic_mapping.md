---
UID: NS:winnt._GENERIC_MAPPING
title: "_GENERIC_MAPPING"
author: windows-sdk-content
description: Defines the mapping of generic access rights to specific and standard access rights for an object.
old-location: security\generic_mapping.htm
old-project: SecAuthZ
ms.assetid: e3c49b47-9bc7-4000-a131-449345ebb9cd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PGENERIC_MAPPING, GENERIC_MAPPING, GENERIC_MAPPING structure [Security], PGENERIC_MAPPING, PGENERIC_MAPPING structure pointer [Security], _GENERIC_MAPPING, _win32_generic_mapping_str, security.generic_mapping, winnt/GENERIC_MAPPING, winnt/PGENERIC_MAPPING"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: GENERIC_MAPPING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - GENERIC_MAPPING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _GENERIC_MAPPING structure


## -description


The <b>GENERIC_MAPPING</b> structure defines the mapping of generic access rights to specific and standard access rights for an object. When a client application requests generic access to an object, that request is mapped to the access rights defined in this structure.


## -struct-fields




### -field GenericRead

Specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> defining read access to an object.


### -field GenericWrite

Specifies an access mask defining write access to an object.


### -field GenericExecute

Specifies an access mask defining execute access to an object.


### -field GenericAll

Specifies an access mask defining all possible types of access to an object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>
 

 

