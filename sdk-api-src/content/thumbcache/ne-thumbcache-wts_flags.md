---
UID: NE:thumbcache.WTS_FLAGS
title: WTS_FLAGS (thumbcache.h)
description: Values used by IThumbnailCache::GetThumbnail to specify options for the extraction and display of the thumbnail image.
helpviewer_keywords: ["WTS_APPSTYLE","WTS_CROPTOSQUARE","WTS_EXTRACT","WTS_EXTRACTDONOTCACHE","WTS_EXTRACTINPROC","WTS_FASTEXTRACT","WTS_FLAGS","WTS_FLAGS enumeration [Windows Shell]","WTS_FORCEEXTRACTION","WTS_IDEALCACHESIZEONLY","WTS_INCACHEONLY","WTS_INSTANCESURROGATE","WTS_NONE","WTS_REQUIRESURROGATE","WTS_SCALETOREQUESTEDSIZE","WTS_SCALEUP","WTS_SKIPFASTEXTRACT","WTS_SLOWRECLAIM","WTS_WIDETHUMBNAILS","shell.WTS_FLAGS","thumbcache/WTS_APPSTYLE","thumbcache/WTS_CROPTOSQUARE","thumbcache/WTS_EXTRACT","thumbcache/WTS_EXTRACTDONOTCACHE","thumbcache/WTS_EXTRACTINPROC","thumbcache/WTS_FASTEXTRACT","thumbcache/WTS_FLAGS","thumbcache/WTS_FORCEEXTRACTION","thumbcache/WTS_IDEALCACHESIZEONLY","thumbcache/WTS_INCACHEONLY","thumbcache/WTS_INSTANCESURROGATE","thumbcache/WTS_NONE","thumbcache/WTS_REQUIRESURROGATE","thumbcache/WTS_SCALETOREQUESTEDSIZE","thumbcache/WTS_SCALEUP","thumbcache/WTS_SKIPFASTEXTRACT","thumbcache/WTS_SLOWRECLAIM","thumbcache/WTS_WIDETHUMBNAILS"]
old-location: shell\WTS_FLAGS.htm
tech.root: shell
ms.assetid: D9C84E86-35AF-437f-966E-BABD02B824C0
ms.date: 12/05/2018
ms.keywords: WTS_APPSTYLE, WTS_CROPTOSQUARE, WTS_EXTRACT, WTS_EXTRACTDONOTCACHE, WTS_EXTRACTINPROC, WTS_FASTEXTRACT, WTS_FLAGS, WTS_FLAGS enumeration [Windows Shell], WTS_FORCEEXTRACTION, WTS_IDEALCACHESIZEONLY, WTS_INCACHEONLY, WTS_INSTANCESURROGATE, WTS_NONE, WTS_REQUIRESURROGATE, WTS_SCALETOREQUESTEDSIZE, WTS_SCALEUP, WTS_SKIPFASTEXTRACT, WTS_SLOWRECLAIM, WTS_WIDETHUMBNAILS, shell.WTS_FLAGS, thumbcache/WTS_APPSTYLE, thumbcache/WTS_CROPTOSQUARE, thumbcache/WTS_EXTRACT, thumbcache/WTS_EXTRACTDONOTCACHE, thumbcache/WTS_EXTRACTINPROC, thumbcache/WTS_FASTEXTRACT, thumbcache/WTS_FLAGS, thumbcache/WTS_FORCEEXTRACTION, thumbcache/WTS_IDEALCACHESIZEONLY, thumbcache/WTS_INCACHEONLY, thumbcache/WTS_INSTANCESURROGATE, thumbcache/WTS_NONE, thumbcache/WTS_REQUIRESURROGATE, thumbcache/WTS_SCALETOREQUESTEDSIZE, thumbcache/WTS_SCALEUP, thumbcache/WTS_SKIPFASTEXTRACT, thumbcache/WTS_SLOWRECLAIM, thumbcache/WTS_WIDETHUMBNAILS
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
req.typenames: WTS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTS_FLAGS
 - thumbcache/WTS_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Thumbcache.h
api_name:
 - WTS_FLAGS
---

# WTS_FLAGS enumeration


## -description

Values used by <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a> to specify options for the extraction and display of the thumbnail image.

## -enum-fields

### -field WTS_NONE:0

0x00000000. <b>Introduced in Windows 8</b>. None of the following options are set.

### -field WTS_EXTRACT:0

Default. 0x00000000. Extract the thumbnail if it is not cached.

### -field WTS_INCACHEONLY:0x1

0x00000001. Only return the thumbnail if it is cached.

### -field WTS_FASTEXTRACT:0x2

0x00000002. If not cached, only extract the thumbnail if it is embedded in EXIF format, typically 96x96.

### -field WTS_FORCEEXTRACTION:0x4

0x00000004. Ignore cache and extract thumbnail from source file.

### -field WTS_SLOWRECLAIM:0x8

0x00000008. The thumbnail has an extended lifetime. Use for volumes that might go offline, like non-fixed disks.

### -field WTS_EXTRACTDONOTCACHE:0x20

0x00000020. Extract but do not add the thumbnail to the cache.

### -field WTS_SCALETOREQUESTEDSIZE:0x40

0x00000040. <b>Introduced in Windows 7</b>. If the specific thumbnail size requested in the <i>cxyRequestedThumbSize</i> parameter is not available, resize the thumbnail to the requested size. If possible, a larger bitmap is reduced in scale, preserving its aspect ratio, to the width and height required. If the only available cached thumbnail is smaller than the requested size, then it is scaled up using the nearest-neighbor algorithm.

### -field WTS_SKIPFASTEXTRACT:0x80

0x00000080. <b>Introduced in Windows 7</b>. Do not extract a thumbnail embedded in the metadata of an EXIF image.

### -field WTS_EXTRACTINPROC:0x100

0x00000100. <b>Introduced in Windows 7</b>. Ensures that the thumbnail handler is loaded in the same process as the caller. When this flag is not specified, the handler is loaded into a surrogate process to protect the caller from unexpected crashes caused by the processing of the target file. Use this value when debugging thumbnail extractors.

### -field WTS_CROPTOSQUARE:0x200

0x00000200. <b>Introduced in Windows 8</b>. If necessary, crop the bitmap's dimensions so that is square. The length of the shortest side becomes the length of all sides.

### -field WTS_INSTANCESURROGATE:0x400

0x00000400. <b>Introduced in Windows 8</b>. Create a surrogate for this instance of the cache rather than using the shared DLLHost surrogate.

### -field WTS_REQUIRESURROGATE:0x800

0x00000800. <b>Introduced in Windows 8</b>. Require extractions to take place in the surrogate.

### -field WTS_APPSTYLE:0x2000

0x00002000. <b>Windows 8 and later</b>. Pass the <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_contextflags">WTSCF_APPSTYLE</a> flag to <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailsettings-setcontext">IThumbnailSettings::SetContext</a>, if the provider supports it.

### -field WTS_WIDETHUMBNAILS:0x4000

0x00004000. <b>Windows 8 and later</b>. Stretch and crop the bitmap so that its height is 0.7 times its width.

### -field WTS_IDEALCACHESIZEONLY:0x8000

0x00008000. <b>Windows 8 and later</b>. Return from the ideal cache snap size only. The returned image might be larger, but it will be pulled from the correct cache entry.

### -field WTS_SCALEUP:0x10000

0x00010000. <b>Windows 8 and later</b>. If necessary, stretch the image so that the height and width fit the given size.

## -remarks

The following combinations are valid.

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

## -see-also

<a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a>



<a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailsettings-setcontext">IThumbnailSettings::SetContext</a>
