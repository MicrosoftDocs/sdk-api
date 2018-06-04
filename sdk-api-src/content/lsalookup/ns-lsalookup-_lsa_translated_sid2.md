---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _LSA_TRANSLATED_SID2 structure


## -description


The <b>LSA_TRANSLATED_SID2</b> structure contains 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SIDs</a> that are retrieved based on account names. This structure is used by the 
<a href="https://msdn.microsoft.com/fe219070-6a00-4b8c-b2e4-2ad290a1cb9c">LsaLookupNames2</a> function.


## -struct-fields




### -field Use

An 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration value that identifies the use of the SID. If this value is SidTypeUnknown or SidTypeInvalid, the rest of the information in the structure is not valid and should be ignored.


### -field Sid

The complete SID of the account.


### -field DomainIndex

The index of an entry in a related 
<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a> data structure which describes the domain that owns the account. If there is no corresponding reference domain for an entry, then <b>DomainIndex</b> will contain a negative value.


### -field Flags

Not used.

