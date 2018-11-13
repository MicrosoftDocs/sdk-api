---
UID: NS:winnt._SID_AND_ATTRIBUTES
title: "_SID_AND_ATTRIBUTES"
author: windows-sdk-content
description: Represents a security identifier (SID) and its attributes.
old-location: security\sid_and_attributes.htm
tech.root: SecAuthZ
ms.assetid: d15d5a3f-6b38-4b92-b59c-ff0d27d111d9
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: "*PSID_AND_ATTRIBUTES, PSID_AND_ATTRIBUTES, PSID_AND_ATTRIBUTES structure pointer [Security], SID_AND_ATTRIBUTES, SID_AND_ATTRIBUTES structure [Security], _SID_AND_ATTRIBUTES, _win32_sid_and_attributes_str, security.sid_and_attributes, winnt/PSID_AND_ATTRIBUTES, winnt/SID_AND_ATTRIBUTES"
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
 - SID_AND_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: SID_AND_ATTRIBUTES, *PSID_AND_ATTRIBUTES
req.redist: 
---

# _SID_AND_ATTRIBUTES structure


## -description


The <b>SID_AND_ATTRIBUTES</b> structure represents a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) and its attributes. SIDs are used to uniquely identify users or groups.


## -struct-fields




### -field Sid

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure.


### -field Attributes

Specifies attributes of the SID. This value contains up to 32 one-bit flags. Its meaning depends on the definition and use of the SID.


## -remarks



A group is represented by a SID. SIDs have attributes that indicate whether they are currently enabled, disabled, or mandatory. SIDs also indicate how these attributes are used. A <b>SID_AND_ATTRIBUTES</b> structure can represent a SID whose attributes change frequently. For example, <b>SID_AND_ATTRIBUTES</b> is used to represent groups in the <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>
 

 

