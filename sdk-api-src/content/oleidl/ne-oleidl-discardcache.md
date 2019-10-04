---
UID: NE:oleidl.tagDISCARDCACHE
title: DISCARDCACHE (oleidl.h)
author: windows-sdk-content
description: Specifies what to do with caches that are to be discarded from memory if their dirty bit has been set.
old-location: com\discardcache.htm
tech.root: com
ms.assetid: 879caecd-8231-449b-8329-e627c85030bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DISCARDCACHE, DISCARDCACHE enumeration [COM], DISCARDCACHE_NOSAVE, DISCARDCACHE_SAVEIFDIRTY, _ole_DISCARDCACHE, com.discardcache, oleidl/DISCARDCACHE, oleidl/DISCARDCACHE_NOSAVE, oleidl/DISCARDCACHE_SAVEIFDIRTY
ms.topic: enum
f1_keywords: 
 - "oleidl/DISCARDCACHE"
dev_langs:
 - c++
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - OleIdl.h
api_name:
 - DISCARDCACHE
targetos: Windows
req.typenames: DISCARDCACHE
req.redist: 
ms.custom: 19H1
---

# DISCARDCACHE enumeration


## -description


Specifies what to do with caches that are to be discarded from memory if their dirty bit has been set.


## -enum-fields




### -field DISCARDCACHE_SAVEIFDIRTY

The cache is to be saved to disk.


### -field DISCARDCACHE_NOSAVE

The cache can be discarded without saving it.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolecache2-discardcache">IOleCache2::DiscardCache</a>
 

 

