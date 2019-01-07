---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0010
title: ResourcePolicy
author: windows-sdk-content
description: Defines how folders are deleted when one of the disk resource limits is exceeded.
old-location: pla\resourcepolicy.htm
tech.root: PLA
ms.assetid: 6dbe0a60-d2f9-4e76-81d9-d9891c08109a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ResourcePolicy, ResourcePolicy enumeration [PLA], base.resourcepolicy, pla.resourcepolicy, pla/ResourcePolicy, pla/plaDeleteLargest, pla/plaDeleteOldest, plaDeleteLargest, plaDeleteOldest
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - ResourcePolicy
product: Windows
targetos: Windows
req.typenames: ResourcePolicy
req.redist: 
---

# ResourcePolicy enumeration


## -description


Defines how folders are deleted when one of the disk resource limits is exceeded. 


## -enum-fields




### -field plaDeleteLargest

Delete folders from largest to smallest.


### -field plaDeleteOldest

Delete folders from oldest to newest.


## -see-also




<a href="https://msdn.microsoft.com/541cd28c-2e01-4b8a-9cd3-044896c8fb80">IDataManager::ResourcePolicy</a>
 

 

