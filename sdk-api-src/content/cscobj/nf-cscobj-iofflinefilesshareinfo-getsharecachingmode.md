---
UID: NF:cscobj.IOfflineFilesShareInfo.GetShareCachingMode
title: IOfflineFilesShareInfo::GetShareCachingMode (cscobj.h)
description: Retrieves the caching mode configuration of the closest ancestor share to the item.
helpviewer_keywords: ["GetShareCachingMode","GetShareCachingMode method [Offline Files]","GetShareCachingMode method [Offline Files]","IOfflineFilesShareInfo interface","IOfflineFilesShareInfo interface [Offline Files]","GetShareCachingMode method","IOfflineFilesShareInfo.GetShareCachingMode","IOfflineFilesShareInfo::GetShareCachingMode","OFFLINEFILES_CACHING_MODE_AUTO_DOC","OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC","OFFLINEFILES_CACHING_MODE_MANUAL","OFFLINEFILES_CACHING_MODE_NOCACHING","OFFLINEFILES_CACHING_MODE_NONE","cscobj/IOfflineFilesShareInfo::GetShareCachingMode","of.iofflinefilesshareinfo_getsharecachingmode"]
old-location: of\iofflinefilesshareinfo_getsharecachingmode.htm
tech.root: of
ms.assetid: 0045497b-0f90-4e20-80c9-6b74e4b523b8
ms.date: 12/05/2018
ms.keywords: GetShareCachingMode, GetShareCachingMode method [Offline Files], GetShareCachingMode method [Offline Files],IOfflineFilesShareInfo interface, IOfflineFilesShareInfo interface [Offline Files],GetShareCachingMode method, IOfflineFilesShareInfo.GetShareCachingMode, IOfflineFilesShareInfo::GetShareCachingMode, OFFLINEFILES_CACHING_MODE_AUTO_DOC, OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, OFFLINEFILES_CACHING_MODE_MANUAL, OFFLINEFILES_CACHING_MODE_NOCACHING, OFFLINEFILES_CACHING_MODE_NONE, cscobj/IOfflineFilesShareInfo::GetShareCachingMode, of.iofflinefilesshareinfo_getsharecachingmode
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
 - IOfflineFilesShareInfo::GetShareCachingMode
 - cscobj/IOfflineFilesShareInfo::GetShareCachingMode
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
 - IOfflineFilesShareInfo.GetShareCachingMode
---

# IOfflineFilesShareInfo::GetShareCachingMode


## -description

Retrieves the caching mode configuration of the closest ancestor share to the item.

## -parameters

### -param pCachingMode [out]

Receives a value from the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_caching_mode">OFFLINEFILES_CACHING_MODE</a> enumeration that indicates the caching mode.

The following values can be returned:



#### OFFLINEFILES_CACHING_MODE_NONE (0)

No caching mode value was found. This value can be returned if the method fails.



#### OFFLINEFILES_CACHING_MODE_NOCACHING (1)

The share is configured to disallow caching. This value corresponds to a value of zero returned by the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_MANUAL (2)

The share is configured to allow manual caching. This value corresponds to a value of <b>CSC_CACHE_MANUAL_REINT</b> returned by the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function for the CSC_MASK portion of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_AUTO_DOC (3)

The share is configured to allow automatic caching of documents. This value corresponds to a value of <b>CSC_CACHE_AUTO_REINT</b> returned by the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC (4)

The share is configured to allow automatic caching of programs and documents. This value corresponds to a value of <b>CSC_CACHE_VDO</b> (virtual disconnected operations) returned by the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> structure.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This method is equivalent to locating the nearest share item, obtaining its fully qualified UNC path and calling <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> for <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> information.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-ispathcacheable">IOfflineFilesCache::IsPathCacheable</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareinfo">IOfflineFilesShareInfo</a>