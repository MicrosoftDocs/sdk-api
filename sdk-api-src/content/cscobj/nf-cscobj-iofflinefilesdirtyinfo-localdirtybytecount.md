---
UID: NF:cscobj.IOfflineFilesDirtyInfo.LocalDirtyByteCount
title: IOfflineFilesDirtyInfo::LocalDirtyByteCount (cscobj.h)
description: Retrieves the amount of unsynchronized (&quot;dirty&quot;) data for the associated file in the local Offline Files cache.
helpviewer_keywords: ["IOfflineFilesDirtyInfo interface [Offline Files]","LocalDirtyByteCount method","IOfflineFilesDirtyInfo.LocalDirtyByteCount","IOfflineFilesDirtyInfo::LocalDirtyByteCount","LocalDirtyByteCount","LocalDirtyByteCount method [Offline Files]","LocalDirtyByteCount method [Offline Files]","IOfflineFilesDirtyInfo interface","cscobj/IOfflineFilesDirtyInfo::LocalDirtyByteCount","of.iofflinefilesdirtyinfo_localdirtybytecount"]
old-location: of\iofflinefilesdirtyinfo_localdirtybytecount.htm
tech.root: of
ms.assetid: c261d5ac-5834-42c7-b644-4244db9d653e
ms.date: 12/05/2018
ms.keywords: IOfflineFilesDirtyInfo interface [Offline Files],LocalDirtyByteCount method, IOfflineFilesDirtyInfo.LocalDirtyByteCount, IOfflineFilesDirtyInfo::LocalDirtyByteCount, LocalDirtyByteCount, LocalDirtyByteCount method [Offline Files], LocalDirtyByteCount method [Offline Files],IOfflineFilesDirtyInfo interface, cscobj/IOfflineFilesDirtyInfo::LocalDirtyByteCount, of.iofflinefilesdirtyinfo_localdirtybytecount
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
 - IOfflineFilesDirtyInfo::LocalDirtyByteCount
 - cscobj/IOfflineFilesDirtyInfo::LocalDirtyByteCount
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
 - IOfflineFilesDirtyInfo.LocalDirtyByteCount
---

# IOfflineFilesDirtyInfo::LocalDirtyByteCount


## -description

Retrieves the amount of unsynchronized ("dirty") data for the associated file in the local Offline Files cache.

## -parameters

### -param pDirtyByteCount [out]

The number of bytes of unsynchronized data.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This method can be called only for file items, which are represented by <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfileitem">IOfflineFilesFileItem</a> objects.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesdirtyinfo">IOfflineFilesDirtyInfo</a>