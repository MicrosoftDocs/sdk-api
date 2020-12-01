---
UID: NF:thumbcache.IThumbnailCache.GetThumbnail
title: IThumbnailCache::GetThumbnail (thumbcache.h)
description: Gets a cached thumbnail for a given Shell item.
helpviewer_keywords: ["GetThumbnail","GetThumbnail method [Windows Shell]","GetThumbnail method [Windows Shell]","IThumbnailCache interface","IThumbnailCache interface [Windows Shell]","GetThumbnail method","IThumbnailCache.GetThumbnail","IThumbnailCache::GetThumbnail","WTS_CACHED","WTS_DEFAULT","WTS_LOWQUALITY","_shell__GetThumbnail","shell.IThumbnailCache_GetThumbnail","thumbcache/IThumbnailCache::GetThumbnail"]
old-location: shell\IThumbnailCache_GetThumbnail.htm
tech.root: shell
ms.assetid: 0fcfe68b-5d36-4be1-a468-b5c2d7af0651
ms.date: 12/05/2018
ms.keywords: GetThumbnail, GetThumbnail method [Windows Shell], GetThumbnail method [Windows Shell],IThumbnailCache interface, IThumbnailCache interface [Windows Shell],GetThumbnail method, IThumbnailCache.GetThumbnail, IThumbnailCache::GetThumbnail, WTS_CACHED, WTS_DEFAULT, WTS_LOWQUALITY, _shell__GetThumbnail, shell.IThumbnailCache_GetThumbnail, thumbcache/IThumbnailCache::GetThumbnail
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
 - IThumbnailCache::GetThumbnail
 - thumbcache/IThumbnailCache::GetThumbnail
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
 - IThumbnailCache.GetThumbnail
---

# IThumbnailCache::GetThumbnail


## -description

Gets a cached thumbnail for a given Shell item.

## -parameters

### -param pShellItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item for which to retrieve a thumbnail.

### -param cxyRequestedThumbSize [in]

Type: <b>UINT</b>

The requested thumbnail size in pixels. The maximum value is 1024.

### -param flags [in]

Type: <b><a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_FLAGS</a></b>

A combination of values from the <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_FLAGS</a> enumeration. See the Remarks section for rules and a list of possible combinations.

### -param ppvThumb [out, optional]

Type: <b><a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a>**</b>

The address of an <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> pointer that, when this method returns successfully, receives the object used to access the thumbnail. This parameter may be <b>NULL</b>.

### -param pOutFlags [out, optional]

Type: <b>WTS_CACHEFLAGS*</b>

A pointer to a value that, when this method returns successfully, receives a combination of the following flags from the WTS_CACHEFLAGS enumeration.



#### WTS_DEFAULT (0x00000000)

0x00000000. 



#### WTS_LOWQUALITY (0x00000001)

0x00000001. Set when the returned bitmap dimensions are less than <i>cxyRequestedThumbSize</i>.



#### WTS_CACHED (0x00000002)

0x00000002. Set when the returned image is in the cache.

### -param pThumbnailID [out, optional]

Type: <b><a href="/windows/desktop/api/thumbcache/ns-thumbcache-wts_thumbnailid">WTS_THUMBNAILID</a>*</b>

A pointer to a value that, when this method returns successfully, receives a unique ID for the returned thumbnail. This parameter may be <b>NULL</b>, in which case the thumbnail ID is discarded.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful or a standard COM error value otherwise, including the following:

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

If a thumbnail is extracted, it will be cached unless WTS_EXTRACTDONOTCACHE is specified.

The following combinations are valid for the flags parameter.

<table class="clsStd">
<tr>
<td>WTS_INCACHEONLY</td>
</tr>
<tr>
<td>WTS_FASTEXTRACT</td>
</tr>
<tr>
<td>WTS_EXTRACT</td>
</tr>
<tr>
<td>WTS_EXTRACT | WTS_SLOWRECLAIM</td>
</tr>
<tr>
<td>WTS_FORCEEXTRACTION</td>
</tr>
<tr>
<td>WTS_FORCEEXTRACTION | WTS_SLOWRECLAIM</td>
</tr>
<tr>
<td>WTS_EXTRACTDONOTCACHE</td>
</tr>
</table>
 


<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemimagefactory-getimage">GetImage</a> also uses this cache and can provide an easier way to retrieve the thumbnail. However, <b>GetImage</b> is more general and will retrieve an icon as a fallback.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemimagefactory-getimage">IShellItemImageFactory::GetImage</a>



<a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcache">IThumbnailCache</a>