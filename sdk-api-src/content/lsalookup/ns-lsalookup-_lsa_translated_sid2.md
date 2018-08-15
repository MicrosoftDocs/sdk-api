---
UID: NS:lsalookup._LSA_TRANSLATED_SID2
title: "_LSA_TRANSLATED_SID2"
author: windows-sdk-content
description: Contains SIDs that are retrieved based on account names.
old-location: security\lsa_translated_sid2.htm
old-project: secmgmt
ms.assetid: 792de958-8e24-46d8-b484-159435bc96e3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLSA_TRANSLATED_SID2, LSA_TRANSLATED_SID2, LSA_TRANSLATED_SID2 structure [Security], PLSA_TRANSLATED_SID2, PLSA_TRANSLATED_SID2 structure pointer [Security], _LSA_TRANSLATED_SID2, _lsa_lsa_translated_sid2, lsalookup/LSA_TRANSLATED_SID2, lsalookup/PLSA_TRANSLATED_SID2, security.lsa_translated_sid2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lsalookup.h
req.include-header: 
req.redist: 
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
req.typenames: LSA_TRANSLATED_SID2, *PLSA_TRANSLATED_SID2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LsaLookup.h
api_name:
 - LSA_TRANSLATED_SID2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LSA_TRANSLATED_SID2 structure


## -description


The <b>LSA_TRANSLATED_SID2</b> structure contains 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SIDs</a> that are retrieved based on account names. This structure is used by the 
<a href="https://msdn.microsoft.com/fe219070-6a00-4b8c-b2e4-2ad290a1cb9c">LsaLookupNames2</a> function.


## -struct-fields




### -field Use

An 
<a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a> enumeration value that identifies the use of the SID. If this value is SidTypeUnknown or SidTypeInvalid, the rest of the information in the structure is not valid and should be ignored.


### -field Sid

The complete SID of the account.


### -field DomainIndex

The index of an entry in a related 
<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a> data structure which describes the domain that owns the account. If there is no corresponding reference domain for an entry, then <b>DomainIndex</b> will contain a negative value.


### -field Flags

Not used.

