---
UID: NF:thumbcache.IThumbnailCache.GetThumbnailByID
title: IThumbnailCache::GetThumbnailByID (thumbcache.h)
description: Gets a thumbnail from the thumbnail cache, given its ID.
helpviewer_keywords: ["GetThumbnailByID","GetThumbnailByID method [Windows Shell]","GetThumbnailByID method [Windows Shell]","IThumbnailCache interface","IThumbnailCache interface [Windows Shell]","GetThumbnailByID method","IThumbnailCache.GetThumbnailByID","IThumbnailCache::GetThumbnailByID","WTS_CACHED","WTS_DEFAULT","WTS_LOWQUALITY","_shell__GetThumbnailByID","shell.IThumbnailCache_GetThumbnailByID","thumbcache/IThumbnailCache::GetThumbnailByID"]
old-location: shell\IThumbnailCache_GetThumbnailByID.htm
tech.root: shell
ms.assetid: 3b5069e2-f20b-4c43-a9e7-334366980f5c
ms.date: 12/05/2018
ms.keywords: GetThumbnailByID, GetThumbnailByID method [Windows Shell], GetThumbnailByID method [Windows Shell],IThumbnailCache interface, IThumbnailCache interface [Windows Shell],GetThumbnailByID method, IThumbnailCache.GetThumbnailByID, IThumbnailCache::GetThumbnailByID, WTS_CACHED, WTS_DEFAULT, WTS_LOWQUALITY, _shell__GetThumbnailByID, shell.IThumbnailCache_GetThumbnailByID, thumbcache/IThumbnailCache::GetThumbnailByID
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IThumbnailCache::GetThumbnailByID
 - thumbcache/IThumbnailCache::GetThumbnailByID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - IThumbnailCache.GetThumbnailByID
---

# IThumbnailCache::GetThumbnailByID


## -description

Gets a thumbnail from the thumbnail cache, given its ID.

## -parameters

### -param thumbnailID [in]

Type: <b><a href="/windows/desktop/api/thumbcache/ns-thumbcache-wts_thumbnailid">WTS_THUMBNAILID</a></b>

The ID of the thumbnail to retrieve. The ID is obtained by calling <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">GetThumbnail</a>.

### -param cxyRequestedThumbSize [in]

Type: <b>UINT</b>

The requested thumbnail size in pixels. This value cannot be larger than 1024.

### -param ppvThumb [out, optional]

Type: <b><a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a>**</b>

The address of a <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> interface pointer that, when this method returns successfully, receives the object for accessing the requested thumbnail. This parameter can be <b>NULL</b>.

### -param pOutFlags [out, optional]

Type: <b>WTS_CACHEFLAGS*</b>

A pointer to a value that, when this method returns successfully, receives a combination of the following flags. This value can be set to <b>NULL</b> if this information is not needed.



#### WTS_DEFAULT (0x00000000)

0x00000000. 



#### WTS_LOWQUALITY (0x00000001)

0x00000001. Set when the returned bitmap dimensions are less than <i>cxyRequestedThumbSize</i>.



#### WTS_CACHED (0x00000002)

0x00000002. Set when the returned image is in the cache.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WTS_E_FAILEDEXTRACTION</b></dt>
</dl>
</td>
<td width="60%">
The Shell item does not support thumbnail extraction. For example, .exe or .lnk items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WTS_E_EXTRACTIONTIMEDOUT</b></dt>
</dl>
</td>
<td width="60%">
The extraction took longer than the maximum allowable time. The extraction was not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WTS_E_SURROGATEUNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
A surrogate process was not available to be used for the extraction process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WTS_E_FASTEXTRACTIONNOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The WTS_FASTEXTRACT flag was set, but fast extraction is not available.

</td>
</tr>
</table>

## -remarks

This method is typically called after <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">GetThumbnail</a> has already been called to retrieve the thumbnail ID.