---
UID: NS:lsalookup._LSA_REFERENCED_DOMAIN_LIST
title: "_LSA_REFERENCED_DOMAIN_LIST"
author: windows-sdk-content
description: The LSA_REFERENCED_DOMAIN_LIST structure contains information about the domains referenced in a lookup operation.
old-location: security\lsa_referenced_domain_list.htm
tech.root: secmgmt
ms.assetid: ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PLSA_REFERENCED_DOMAIN_LIST, LSA_REFERENCED_DOMAIN_LIST, LSA_REFERENCED_DOMAIN_LIST structure [Security], PLSA_REFERENCED_DOMAIN_LIST, PLSA_REFERENCED_DOMAIN_LIST structure pointer [Security], _LSA_REFERENCED_DOMAIN_LIST, _lsa_lsa_referenced_domain_list, lsalookup/LSA_REFERENCED_DOMAIN_LIST, lsalookup/PLSA_REFERENCED_DOMAIN_LIST, security.lsa_referenced_domain_list"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lsalookup.h
req.include-header: 
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
 - lsalookup.h
api_name:
 - LSA_REFERENCED_DOMAIN_LIST
product: Windows
targetos: Windows
req.typenames: LSA_REFERENCED_DOMAIN_LIST, *PLSA_REFERENCED_DOMAIN_LIST
req.redist: 
---

# _LSA_REFERENCED_DOMAIN_LIST structure


## -description


The <b>LSA_REFERENCED_DOMAIN_LIST</b> structure contains information about the domains referenced in a lookup operation.


## -struct-fields




### -field Entries

Specifies the number of entries in the <b>Domains</b> array.


### -field Domains

Pointer to an array of 
<a href="https://msdn.microsoft.com/2b5e6f79-b97a-4018-a45a-37c300c3dc0d">LSA_TRUST_INFORMATION</a> structures that identify the referenced domains.


## -see-also




<a href="https://msdn.microsoft.com/2b5e6f79-b97a-4018-a45a-37c300c3dc0d">LSA_TRUST_INFORMATION</a>



<a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a>



<a href="https://msdn.microsoft.com/69051bad-91e7-469d-9010-48ac3d20f8af">LsaLookupSids</a>
 

 

