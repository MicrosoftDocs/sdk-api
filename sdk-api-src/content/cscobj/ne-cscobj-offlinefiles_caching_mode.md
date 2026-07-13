---
UID: NE:cscobj.tagOFFLINEFILES_CACHING_MODE
title: OFFLINEFILES_CACHING_MODE (cscobj.h)
description: Describes the caching mode used in methods such as IOfflineFilesCache::IsPathCacheable and IOfflineFilesShareInfo::GetShareCachingMode.
helpviewer_keywords: ["OFFLINEFILES_CACHING_MODE","OFFLINEFILES_CACHING_MODE enumeration [Offline Files]","OFFLINEFILES_CACHING_MODE_AUTO_DOC","OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC","OFFLINEFILES_CACHING_MODE_MANUAL","OFFLINEFILES_CACHING_MODE_NOCACHING","OFFLINEFILES_CACHING_MODE_NONE","cscobj/OFFLINEFILES_CACHING_MODE","cscobj/OFFLINEFILES_CACHING_MODE_AUTO_DOC","cscobj/OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC","cscobj/OFFLINEFILES_CACHING_MODE_MANUAL","cscobj/OFFLINEFILES_CACHING_MODE_NOCACHING","cscobj/OFFLINEFILES_CACHING_MODE_NONE","of.offlinefiles_caching_mode"]
old-location: of\offlinefiles_caching_mode.htm
tech.root: of
ms.assetid: 833cd194-7086-4faa-a05b-5f8beda62f0a
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_CACHING_MODE, OFFLINEFILES_CACHING_MODE enumeration [Offline Files], OFFLINEFILES_CACHING_MODE_AUTO_DOC, OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, OFFLINEFILES_CACHING_MODE_MANUAL, OFFLINEFILES_CACHING_MODE_NOCACHING, OFFLINEFILES_CACHING_MODE_NONE, cscobj/OFFLINEFILES_CACHING_MODE, cscobj/OFFLINEFILES_CACHING_MODE_AUTO_DOC, cscobj/OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, cscobj/OFFLINEFILES_CACHING_MODE_MANUAL, cscobj/OFFLINEFILES_CACHING_MODE_NOCACHING, cscobj/OFFLINEFILES_CACHING_MODE_NONE, of.offlinefiles_caching_mode
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFFLINEFILES_CACHING_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_CACHING_MODE
 - cscobj/tagOFFLINEFILES_CACHING_MODE
 - OFFLINEFILES_CACHING_MODE
 - cscobj/OFFLINEFILES_CACHING_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_CACHING_MODE
---

# OFFLINEFILES_CACHING_MODE enumeration


## -description

Describes the caching mode used in methods such as <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-ispathcacheable">IOfflineFilesCache::IsPathCacheable</a> and <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesshareinfo-getsharecachingmode">IOfflineFilesShareInfo::GetShareCachingMode</a>.

## -enum-fields

### -field OFFLINEFILES_CACHING_MODE_NONE:0

No caching mode value was found.

### -field OFFLINEFILES_CACHING_MODE_NOCACHING

The share or shared folder is configured to disallow caching.

### -field OFFLINEFILES_CACHING_MODE_MANUAL

The share or shared folder is configured to allow manual caching.

### -field OFFLINEFILES_CACHING_MODE_AUTO_DOC

The share or shared folder is configured to allow automatic caching of documents.

### -field OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC

The share or shared folder is configured to allow automatic caching of programs and documents.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-ispathcacheable">IOfflineFilesCache::IsPathCacheable</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesshareinfo-getsharecachingmode">IOfflineFilesShareInfo::GetShareCachingMode</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a>
