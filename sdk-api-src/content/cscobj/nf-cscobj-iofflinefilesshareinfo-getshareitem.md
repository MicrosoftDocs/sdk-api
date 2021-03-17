---
UID: NF:cscobj.IOfflineFilesShareInfo.GetShareItem
title: IOfflineFilesShareInfo::GetShareItem (cscobj.h)
description: Finds the cache item representing the closest ancestor share to the item.
helpviewer_keywords: ["GetShareItem","GetShareItem method [Offline Files]","GetShareItem method [Offline Files]","IOfflineFilesShareInfo interface","IOfflineFilesShareInfo interface [Offline Files]","GetShareItem method","IOfflineFilesShareInfo.GetShareItem","IOfflineFilesShareInfo::GetShareItem","cscobj/IOfflineFilesShareInfo::GetShareItem","of.iofflinefilesshareinfo_getshareitem"]
old-location: of\iofflinefilesshareinfo_getshareitem.htm
tech.root: of
ms.assetid: fd4f92fb-1147-4be4-a61d-04f2f371b6c6
ms.date: 12/05/2018
ms.keywords: GetShareItem, GetShareItem method [Offline Files], GetShareItem method [Offline Files],IOfflineFilesShareInfo interface, IOfflineFilesShareInfo interface [Offline Files],GetShareItem method, IOfflineFilesShareInfo.GetShareItem, IOfflineFilesShareInfo::GetShareItem, cscobj/IOfflineFilesShareInfo::GetShareItem, of.iofflinefilesshareinfo_getshareitem
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
 - IOfflineFilesShareInfo::GetShareItem
 - cscobj/IOfflineFilesShareInfo::GetShareItem
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
 - IOfflineFilesShareInfo.GetShareItem
---

# IOfflineFilesShareInfo::GetShareItem


## -description

Finds the cache item representing the closest ancestor share to the item. In non-DFS scenarios this can be the \\server\share at the top of the namespace.  In DFS scenarios this might be a cache directory entry that corresponds to a share in the DFS namespace.

## -parameters

### -param ppShareItem [out]

Receives the address of the <a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareitem">IOfflineFilesShareItem</a> interface on the share item.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareinfo">IOfflineFilesShareInfo</a>