---
UID: NF:cscobj.IOfflineFilesFileSysInfo.GetFileSize
title: IOfflineFilesFileSysInfo::GetFileSize
author: windows-sdk-content
description: Retrieves the size of an item.
old-location: of\iofflinefilesfilesysinfo_getfilesize.htm
tech.root: OfflineFiles
ms.assetid: a24b7126-ee9a-40f8-9fcd-8696e756a6b9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFileSize, GetFileSize method [Offline Files], GetFileSize method [Offline Files],IOfflineFilesFileSysInfo interface, IOfflineFilesFileSysInfo interface [Offline Files],GetFileSize method, IOfflineFilesFileSysInfo.GetFileSize, IOfflineFilesFileSysInfo::GetFileSize, cscobj/IOfflineFilesFileSysInfo::GetFileSize, of.iofflinefilesfilesysinfo_getfilesize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesFileSysInfo.GetFileSize
: 
---

# IOfflineFilesFileSysInfo::GetFileSize


## -description


Retrieves the size of an item.


## -parameters




### -param copy [in]

An <a href="https://msdn.microsoft.com/b956f186-962b-457e-9c03-ffd1a7f937ca">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the size of.

<b>Windows Vista:  </b>This value must be <b>OFFLINEFILES_ITEM_COPY_LOCAL</b>.


### -param pSize [out]

Receive the size, in bytes, of the item.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d3da183d-eb12-4411-b461-b58689ef5bff">IOfflineFilesFileSysInfo</a>
 

 

