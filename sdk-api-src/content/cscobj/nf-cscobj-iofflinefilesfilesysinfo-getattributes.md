---
UID: NF:cscobj.IOfflineFilesFileSysInfo.GetAttributes
title: IOfflineFilesFileSysInfo::GetAttributes (cscobj.h)
description: Retrieves the Win32 attributes for an item.
helpviewer_keywords: ["GetAttributes","GetAttributes method [Offline Files]","GetAttributes method [Offline Files]","IOfflineFilesFileSysInfo interface","IOfflineFilesFileSysInfo interface [Offline Files]","GetAttributes method","IOfflineFilesFileSysInfo.GetAttributes","IOfflineFilesFileSysInfo::GetAttributes","cscobj/IOfflineFilesFileSysInfo::GetAttributes","of.iofflinefilesfilesysinfo_getattributes"]
old-location: of\iofflinefilesfilesysinfo_getattributes.htm
tech.root: of
ms.assetid: 5bf8a834-cd5e-46b9-9b7d-b5cc6fb9fe10
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [Offline Files], GetAttributes method [Offline Files],IOfflineFilesFileSysInfo interface, IOfflineFilesFileSysInfo interface [Offline Files],GetAttributes method, IOfflineFilesFileSysInfo.GetAttributes, IOfflineFilesFileSysInfo::GetAttributes, cscobj/IOfflineFilesFileSysInfo::GetAttributes, of.iofflinefilesfilesysinfo_getattributes
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
 - IOfflineFilesFileSysInfo::GetAttributes
 - cscobj/IOfflineFilesFileSysInfo::GetAttributes
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
 - IOfflineFilesFileSysInfo.GetAttributes
---

# IOfflineFilesFileSysInfo::GetAttributes


## -description

Retrieves the Win32 attributes for an item.

## -parameters

### -param copy [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_copy">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the attributes for.

<b>Windows Vista:  </b>This value must be <b>OFFLINEFILES_ITEM_COPY_LOCAL</b>.

### -param pdwAttributes [out]

Receives the file attribute mask for the item.  One or more of <b>FILE_ATTRIBUTE_<i>XXXXXX</i></b> as defined in the Windows SDK. For more information, see the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> function.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfilesysinfo">IOfflineFilesFileSysInfo</a>