---
UID: NF:cscobj.IOfflineFilesItem.GetPath
title: IOfflineFilesItem::GetPath (cscobj.h)
description: Retrieves the fully qualified UNC path string for an item in the Offline Files cache.
helpviewer_keywords: ["GetPath","GetPath method [Offline Files]","GetPath method [Offline Files]","IOfflineFilesItem interface","IOfflineFilesItem interface [Offline Files]","GetPath method","IOfflineFilesItem.GetPath","IOfflineFilesItem::GetPath","cscobj/IOfflineFilesItem::GetPath","of.iofflinefilesitem_getpath"]
old-location: of\iofflinefilesitem_getpath.htm
tech.root: of
ms.assetid: d1453c9c-e0e7-4451-bb42-58a627fa1db5
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [Offline Files], GetPath method [Offline Files],IOfflineFilesItem interface, IOfflineFilesItem interface [Offline Files],GetPath method, IOfflineFilesItem.GetPath, IOfflineFilesItem::GetPath, cscobj/IOfflineFilesItem::GetPath, of.iofflinefilesitem_getpath
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
 - IOfflineFilesItem::GetPath
 - cscobj/IOfflineFilesItem::GetPath
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
 - IOfflineFilesItem.GetPath
---

# IOfflineFilesItem::GetPath


## -description

Retrieves the fully qualified UNC path string for an item in the Offline Files cache.

## -parameters

### -param ppszPath [out]

Receives the fully qualified UNC path of the item.  The caller is responsible for freeing the path buffer by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>