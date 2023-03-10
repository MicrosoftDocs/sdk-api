---
UID: NF:cscobj.IOfflineFilesShareInfo.IsShareDfsJunction
title: IOfflineFilesShareInfo::IsShareDfsJunction (cscobj.h)
description: Determines whether the share item is a DFS junction or a shared folder on a server.
helpviewer_keywords: ["IOfflineFilesShareInfo interface [Offline Files]","IsShareDfsJunction method","IOfflineFilesShareInfo.IsShareDfsJunction","IOfflineFilesShareInfo::IsShareDfsJunction","IsShareDfsJunction","IsShareDfsJunction method [Offline Files]","IsShareDfsJunction method [Offline Files]","IOfflineFilesShareInfo interface","cscobj/IOfflineFilesShareInfo::IsShareDfsJunction","of.iofflinefilesshareinfo_issharedfsjunction"]
old-location: of\iofflinefilesshareinfo_issharedfsjunction.htm
tech.root: of
ms.assetid: fdb29270-2fe5-4313-afd9-c21b82b1949a
ms.date: 12/05/2018
ms.keywords: IOfflineFilesShareInfo interface [Offline Files],IsShareDfsJunction method, IOfflineFilesShareInfo.IsShareDfsJunction, IOfflineFilesShareInfo::IsShareDfsJunction, IsShareDfsJunction, IsShareDfsJunction method [Offline Files], IsShareDfsJunction method [Offline Files],IOfflineFilesShareInfo interface, cscobj/IOfflineFilesShareInfo::IsShareDfsJunction, of.iofflinefilesshareinfo_issharedfsjunction
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
 - IOfflineFilesShareInfo::IsShareDfsJunction
 - cscobj/IOfflineFilesShareInfo::IsShareDfsJunction
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
 - IOfflineFilesShareInfo.IsShareDfsJunction
---

# IOfflineFilesShareInfo::IsShareDfsJunction


## -description

Determines whether the share item is a DFS junction or a shared folder on a server.

## -parameters

### -param pbIsDfsJunction [out]

Receives <b>TRUE</b> if the item is a DFS junction, or <b>FALSE</b> if the share is a shared folder (\\server\share) on a server.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareinfo">IOfflineFilesShareInfo</a>