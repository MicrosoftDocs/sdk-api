---
UID: NS:winnt._LUID_AND_ATTRIBUTES
title: "_LUID_AND_ATTRIBUTES"
author: windows-sdk-content
description: Represents a locally unique identifier (LUID) and its attributes.
old-location: security\luid_and_attributes.htm
tech.root: secauthz
ms.assetid: f337b561-4b67-42a0-b8de-06f546bafb26
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PLUID_AND_ATTRIBUTES, LUID_AND_ATTRIBUTES, LUID_AND_ATTRIBUTES structure [Security], PLUID_AND_ATTRIBUTES, PLUID_AND_ATTRIBUTES structure pointer [Security], _LUID_AND_ATTRIBUTES, _win32_luid_and_attributes_str, security.luid_and_attributes, winnt/LUID_AND_ATTRIBUTES, winnt/PLUID_AND_ATTRIBUTES"
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
 - LUID_AND_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: LUID_AND_ATTRIBUTES, *PLUID_AND_ATTRIBUTES
req.redist: 
---

# _LUID_AND_ATTRIBUTES structure


## -description


The <b>LUID_AND_ATTRIBUTES</b> structure represents a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID) and its attributes.


## -struct-fields




### -field Luid

Specifies an <a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> value.


### -field Attributes

Specifies attributes of the LUID. This value contains up to 32 one-bit flags. Its meaning is dependent on the definition and use of the LUID.


## -remarks



An <b>LUID_AND_ATTRIBUTES</b> structure can represent an LUID whose attributes change frequently, such as when the LUID is used to represent privileges in the <a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a> structure. Privileges are represented by LUIDs and have attributes indicating whether they are currently enabled or disabled.




## -see-also




<a href="https://msdn.microsoft.com/5d730034-802b-4d37-bd28-68992779b93e">AllocateLocallyUniqueId</a>



<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a>



<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a>
 

 

