---
UID: NF:cscobj.IOfflineFilesFileItem.IsEncrypted
title: IOfflineFilesFileItem::IsEncrypted (cscobj.h)
description: Determines whether an item in the Offline Files cache is encrypted.
helpviewer_keywords: ["IOfflineFilesFileItem interface [Offline Files]","IsEncrypted method","IOfflineFilesFileItem.IsEncrypted","IOfflineFilesFileItem::IsEncrypted","IsEncrypted","IsEncrypted method [Offline Files]","IsEncrypted method [Offline Files]","IOfflineFilesFileItem interface","cscobj/IOfflineFilesFileItem::IsEncrypted","of.iofflinefilesfileitem_isencrypted"]
old-location: of\iofflinefilesfileitem_isencrypted.htm
tech.root: of
ms.assetid: f4ef4836-378c-4a9b-a805-e576d4637a2a
ms.date: 12/05/2018
ms.keywords: IOfflineFilesFileItem interface [Offline Files],IsEncrypted method, IOfflineFilesFileItem.IsEncrypted, IOfflineFilesFileItem::IsEncrypted, IsEncrypted, IsEncrypted method [Offline Files], IsEncrypted method [Offline Files],IOfflineFilesFileItem interface, cscobj/IOfflineFilesFileItem::IsEncrypted, of.iofflinefilesfileitem_isencrypted
f1_keywords:
- cscobj/IOfflineFilesFileItem.IsEncrypted
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CscSvc.dll
- CscObj.dll
api_name:
- IOfflineFilesFileItem.IsEncrypted
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesFileItem::IsEncrypted


## -description


Determines whether an item in the Offline Files cache is encrypted.


## -parameters




### -param pbIsEncrypted [out]

Receives <b>TRUE</b> if the item is encrypted, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfileitem">IOfflineFilesFileItem</a>
 

 

