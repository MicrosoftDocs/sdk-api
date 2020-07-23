---
UID: NF:cscobj.IOfflineFilesFileSysInfo.GetFileSize
title: IOfflineFilesFileSysInfo::GetFileSize (cscobj.h)
description: Retrieves the size of an item.
helpviewer_keywords: ["GetFileSize","GetFileSize method [Offline Files]","GetFileSize method [Offline Files]","IOfflineFilesFileSysInfo interface","IOfflineFilesFileSysInfo interface [Offline Files]","GetFileSize method","IOfflineFilesFileSysInfo.GetFileSize","IOfflineFilesFileSysInfo::GetFileSize","cscobj/IOfflineFilesFileSysInfo::GetFileSize","of.iofflinefilesfilesysinfo_getfilesize"]
old-location: of\iofflinefilesfilesysinfo_getfilesize.htm
tech.root: of
ms.assetid: a24b7126-ee9a-40f8-9fcd-8696e756a6b9
ms.date: 12/05/2018
ms.keywords: GetFileSize, GetFileSize method [Offline Files], GetFileSize method [Offline Files],IOfflineFilesFileSysInfo interface, IOfflineFilesFileSysInfo interface [Offline Files],GetFileSize method, IOfflineFilesFileSysInfo.GetFileSize, IOfflineFilesFileSysInfo::GetFileSize, cscobj/IOfflineFilesFileSysInfo::GetFileSize, of.iofflinefilesfilesysinfo_getfilesize
f1_keywords:
- cscobj/IOfflineFilesFileSysInfo.GetFileSize
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
- IOfflineFilesFileSysInfo.GetFileSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesFileSysInfo::GetFileSize


## -description


Retrieves the size of an item.


## -parameters




### -param copy [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_copy">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the size of.

<b>Windows Vista:  </b>This value must be <b>OFFLINEFILES_ITEM_COPY_LOCAL</b>.


### -param pSize [out]

Receive the size, in bytes, of the item.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfilesysinfo">IOfflineFilesFileSysInfo</a>
 

 

