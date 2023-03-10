---
UID: NF:cscobj.IOfflineFilesItemFilter.GetFilterFlags
title: IOfflineFilesItemFilter::GetFilterFlags (cscobj.h)
description: Provides flags to control flag-based filtering of items.
helpviewer_keywords: ["GetFilterFlags","GetFilterFlags method [Offline Files]","GetFilterFlags method [Offline Files]","IOfflineFilesItemFilter interface","IOfflineFilesItemFilter interface [Offline Files]","GetFilterFlags method","IOfflineFilesItemFilter.GetFilterFlags","IOfflineFilesItemFilter::GetFilterFlags","cscobj/IOfflineFilesItemFilter::GetFilterFlags","of.iofflinefilesitemfilter_getfilterflags"]
old-location: of\iofflinefilesitemfilter_getfilterflags.htm
tech.root: of
ms.assetid: 75466fc7-d14c-4ce7-82e9-9622287a50d1
ms.date: 12/05/2018
ms.keywords: GetFilterFlags, GetFilterFlags method [Offline Files], GetFilterFlags method [Offline Files],IOfflineFilesItemFilter interface, IOfflineFilesItemFilter interface [Offline Files],GetFilterFlags method, IOfflineFilesItemFilter.GetFilterFlags, IOfflineFilesItemFilter::GetFilterFlags, cscobj/IOfflineFilesItemFilter::GetFilterFlags, of.iofflinefilesitemfilter_getfilterflags
req.header: cscobj.h
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesItemFilter::GetFilterFlags
 - cscobj/IOfflineFilesItemFilter::GetFilterFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItemFilter.GetFilterFlags
---

# IOfflineFilesItemFilter::GetFilterFlags


## -description

Provides flags to control flag-based filtering of items.

## -parameters

### -param pullFlags [out]

Receives the <a href="/previous-versions/windows/desktop/offlinefiles/offline-files-filter-flags">Offline Files Filter Flags</a> 
       bit values to be used in the filter evaluation.

A bit value of 1 means that the corresponding data condition in the item must be 
       <b>TRUE</b> for a filter match.  A bit value of 0 means the corresponding data condition in 
       the item must be <b>FALSE</b> for a filter match.

### -param pullMask [out]

Receives the <a href="/previous-versions/windows/desktop/offlinefiles/offline-files-filter-flags">Offline Files Filter Flags</a> 
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

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemfilter">IOfflineFilesItemFilter</a>