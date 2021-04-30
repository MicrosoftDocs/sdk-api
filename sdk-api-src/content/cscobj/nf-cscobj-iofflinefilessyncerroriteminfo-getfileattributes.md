---
UID: NF:cscobj.IOfflineFilesSyncErrorItemInfo.GetFileAttributes
title: IOfflineFilesSyncErrorItemInfo::GetFileAttributes (cscobj.h)
description: Retrieves the Win32 file attributes for the item.
helpviewer_keywords: ["GetFileAttributes","GetFileAttributes method [Offline Files]","GetFileAttributes method [Offline Files]","IOfflineFilesSyncErrorItemInfo interface","IOfflineFilesSyncErrorItemInfo interface [Offline Files]","GetFileAttributes method","IOfflineFilesSyncErrorItemInfo.GetFileAttributes","IOfflineFilesSyncErrorItemInfo::GetFileAttributes","cscobj/IOfflineFilesSyncErrorItemInfo::GetFileAttributes","of.iofflinefilessyncerroriteminfo_getfileattributes"]
old-location: of\iofflinefilessyncerroriteminfo_getfileattributes.htm
tech.root: of
ms.assetid: 4e14d571-230b-4757-8e81-2fb8dc6b9c3f
ms.date: 12/05/2018
ms.keywords: GetFileAttributes, GetFileAttributes method [Offline Files], GetFileAttributes method [Offline Files],IOfflineFilesSyncErrorItemInfo interface, IOfflineFilesSyncErrorItemInfo interface [Offline Files],GetFileAttributes method, IOfflineFilesSyncErrorItemInfo.GetFileAttributes, IOfflineFilesSyncErrorItemInfo::GetFileAttributes, cscobj/IOfflineFilesSyncErrorItemInfo::GetFileAttributes, of.iofflinefilessyncerroriteminfo_getfileattributes
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
 - IOfflineFilesSyncErrorItemInfo::GetFileAttributes
 - cscobj/IOfflineFilesSyncErrorItemInfo::GetFileAttributes
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
 - IOfflineFilesSyncErrorItemInfo.GetFileAttributes
---

# IOfflineFilesSyncErrorItemInfo::GetFileAttributes


## -description

Retrieves the Win32 file attributes for the item.

## -parameters

### -param pdwAttributes [out]

Receives the file attribute mask for the item.  One or more of FILE_ATTRIBUTE_XXXXXX as defined in the Windows SDK. For more information, see the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> function.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a>