---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsLocallyModifiedAttributes
title: IOfflineFilesChangeInfo::IsLocallyModifiedAttributes (cscobj.h)
description: Determines whether one or more of an item's attributes were modified while working offline.
helpviewer_keywords: ["IOfflineFilesChangeInfo interface [Offline Files]","IsLocallyModifiedAttributes method","IOfflineFilesChangeInfo.IsLocallyModifiedAttributes","IOfflineFilesChangeInfo::IsLocallyModifiedAttributes","IsLocallyModifiedAttributes","IsLocallyModifiedAttributes method [Offline Files]","IsLocallyModifiedAttributes method [Offline Files]","IOfflineFilesChangeInfo interface","cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedAttributes","of.iofflinefileschangeinfo_islocallymodifiedattributes"]
old-location: of\iofflinefileschangeinfo_islocallymodifiedattributes.htm
tech.root: of
ms.assetid: c45a04cd-a1cf-4239-9a77-07b6b67121e8
ms.date: 12/05/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsLocallyModifiedAttributes method, IOfflineFilesChangeInfo.IsLocallyModifiedAttributes, IOfflineFilesChangeInfo::IsLocallyModifiedAttributes, IsLocallyModifiedAttributes, IsLocallyModifiedAttributes method [Offline Files], IsLocallyModifiedAttributes method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedAttributes, of.iofflinefileschangeinfo_islocallymodifiedattributes
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
 - IOfflineFilesChangeInfo::IsLocallyModifiedAttributes
 - cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedAttributes
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
 - IOfflineFilesChangeInfo.IsLocallyModifiedAttributes
---

# IOfflineFilesChangeInfo::IsLocallyModifiedAttributes


## -description

Determines whether one or more of an item's attributes were modified while working offline.

## -parameters

### -param pbLocallyModifiedAttributes [out]

Receives <b>TRUE</b> if one or more of the item's attributes were modified in the Offline Files cache while working offline, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

Use <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesfilesysinfo-getattributes">IOfflineFilesFileSysInfo::GetAttributes</a> to examine the Win32 file attributes for an item.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileschangeinfo">IOfflineFilesChangeInfo</a>