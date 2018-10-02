---
UID: NF:mmc.IResultOwnerData.CacheHint
title: IResultOwnerData::CacheHint
author: windows-sdk-content
description: Called when a virtual list is about to request display information for a range of items, allowing the snap-in to collect the information ahead of time in cases where an optimization can be made.
old-location: mmc\iresultownerdata_cachehint.htm
tech.root: MMC
ms.assetid: 8d63e5d7-f342-409a-abea-0305129ba060
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CacheHint, CacheHint method [MMC], CacheHint method [MMC],IResultOwnerData interface, IResultOwnerData interface [MMC],CacheHint method, IResultOwnerData.CacheHint, IResultOwnerData::CacheHint, _slate_iresultownerdata_cachehint, mmc.iresultownerdata_cachehint, mmc/IResultOwnerData::CacheHint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultOwnerData.CacheHint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultOwnerData::CacheHint


## -description


The <b>IResultOwnerData::CacheHint</b> method is called when a virtual list is about to request display information for a range of items, allowing the snap-in to collect the information ahead of time in cases where an optimization can be made.


## -parameters




### -param nStartIndex [in]

An index of the first item to be requested.


### -param nEndIndex [in]

An index of the last item to be requested.


## -returns



This method can return one of these values.




## -remarks



MMC calls 
CacheHint for a virtual list view to assist in optimizing how the snap-in caches requested item data to improve retrieval performance. The arguments passed in the call provide inclusive index values for a range of items that MMC recommends be cached. When 
CacheHint is called, the snap-in must be prepared to load the cache with item information for the requested range so that the information will be readily available when its 
<a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">IComponent::GetDisplayInfo</a> method is called later.

There is no certainty that all the items will be requested or that other items will not be requested.



