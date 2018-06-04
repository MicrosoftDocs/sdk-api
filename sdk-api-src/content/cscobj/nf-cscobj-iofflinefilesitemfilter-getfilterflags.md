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

# IOfflineFilesItemFilter::GetFilterFlags


## -description



    Provides flags to control flag-based filtering of items.
    
   


## -parameters




### -param pullFlags [out]

Receives the <a href="https://msdn.microsoft.com/496126e0-d29b-415c-a3b3-44bdd9e71f78">Offline Files Filter Flags</a> 
       bit values to be used in the filter evaluation.

A bit value of 1 means that the corresponding data condition in the item must be 
       <b>TRUE</b> for a filter match.  A bit value of 0 means the corresponding data condition in 
       the item must be <b>FALSE</b> for a filter match.


### -param pullMask [out]

Receives the <a href="https://msdn.microsoft.com/496126e0-d29b-415c-a3b3-44bdd9e71f78">Offline Files Filter Flags</a> 
       bit values identifying which flags are to be evaluated.

A bit value of 1 means "evaluate the corresponding data" while a bit value of 0 means 
       "do not evaluate the corresponding data."


## -returns



Returns <b>S_OK</b> if the filter supports flag filtering and the flag filtering 
       information is provided.

Returns <b>E_NOTIMPL</b> if flag filtering is not supported.

Any other error value causes the creation of the enumerator to fail.




## -remarks



The combination of bit value and bitmask produces a relatively flexible mechanism for including and excluding 
    items from enumeration. For example, if the <b>OFFLINEFILES_ITEM_FILTER_FLAG_DIRECTORY</b> flag 
    is set in both the <i>pullFlags</i> and <i>pullMask</i> parameters, the 
    matching item must be a directory. If the <b>OFFLINEFILES_ITEM_FILTER_FLAG_DIRECTORY</b> flag 
    is set in the <i>pullMask</i> parameter but is not set in the 
    <i>pullFlags</i> parameter, the matching item must not be a directory.

This method can be implemented in any filter type (inclusion or exclusion) or filter target (file or 
    container).




## -see-also




<a href="https://msdn.microsoft.com/e77b4f90-7a08-47f8-b297-8c1360167e1f">IOfflineFilesItemFilter</a>
 

 

