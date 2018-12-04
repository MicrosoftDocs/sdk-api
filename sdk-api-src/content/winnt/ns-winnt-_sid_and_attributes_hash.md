---
UID: NS:winnt._SID_AND_ATTRIBUTES_HASH
title: "_SID_AND_ATTRIBUTES_HASH"
author: windows-sdk-content
description: Specifies a hash values for the specified array of security identifiers (SIDs).
old-location: security\sid_and_attributes_hash.htm
tech.root: secauthz
ms.assetid: ef6e32f5-b47e-463e-a447-bed149b8d616
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PSID_AND_ATTRIBUTES_HASH, PSID_AND_ATTRIBUTES_HASH, PSID_AND_ATTRIBUTES_HASH structure pointer [Security], SID_AND_ATTRIBUTES_HASH, SID_AND_ATTRIBUTES_HASH structure [Security], _SID_AND_ATTRIBUTES_HASH, security.sid_and_attributes_hash, winnt/PSID_AND_ATTRIBUTES_HASH, winnt/SID_AND_ATTRIBUTES_HASH"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Winnt.h
api_name:
 - SID_AND_ATTRIBUTES_HASH
product: Windows
targetos: Windows
req.typenames: SID_AND_ATTRIBUTES_HASH, *PSID_AND_ATTRIBUTES_HASH
req.redist: 
---

# _SID_AND_ATTRIBUTES_HASH structure


## -description


The <b>SID_AND_ATTRIBUTES_HASH</b> structure specifies a hash values for the specified array of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).


## -struct-fields




### -field SidCount

The number of SIDs pointed to by the <i>SidAttr</i> parameter.


### -field SidAttr

A pointer to an array of <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures that represent SIDs and their attributes.


### -field Hash

An array of pointers to hash values. These values correspond to the <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures pointed to by the <i>SidAttr</i> parameter.

The <b>SID_HASH_ENTRY</b> data type is defined in Winnt.h as a <b>ULONG_PTR</b>.

The <b>SID_HASH_SIZE</b> array dimension is defined in Winnt.h as 32.


## -see-also




<a href="https://msdn.microsoft.com/cb727b91-c88f-48f3-8329-020d3f727dc7">TOKEN_ACCESS_INFORMATION</a>



<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>
 

 

