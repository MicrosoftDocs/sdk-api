---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0010
title: ResourcePolicy (pla.h)
description: Defines how folders are deleted when one of the disk resource limits is exceeded.
helpviewer_keywords: ["ResourcePolicy","ResourcePolicy enumeration [PLA]","base.resourcepolicy","pla.resourcepolicy","pla/ResourcePolicy","pla/plaDeleteLargest","pla/plaDeleteOldest","plaDeleteLargest","plaDeleteOldest"]
old-location: pla\resourcepolicy.htm
tech.root: PLA
ms.assetid: 6dbe0a60-d2f9-4e76-81d9-d9891c08109a
ms.date: 12/05/2018
ms.keywords: ResourcePolicy, ResourcePolicy enumeration [PLA], base.resourcepolicy, pla.resourcepolicy, pla/ResourcePolicy, pla/plaDeleteLargest, pla/plaDeleteOldest, plaDeleteLargest, plaDeleteOldest
req.header: pla.h
req.include-header: 
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
targetos: Windows
req.typenames: ResourcePolicy
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0010
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0010
 - ResourcePolicy
 - pla/ResourcePolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - ResourcePolicy
---

# ResourcePolicy enumeration


## -description

Defines how folders are deleted when one of the disk resource limits is exceeded.

## -enum-fields

### -field plaDeleteLargest:0

Delete folders from largest to smallest.

### -field plaDeleteOldest:1

Delete folders from oldest to newest.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_resourcepolicy">IDataManager::ResourcePolicy</a>
