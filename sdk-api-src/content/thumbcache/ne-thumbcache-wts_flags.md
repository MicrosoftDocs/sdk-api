---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WTS_FLAGS enumeration


## -description


Values used by <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> to specify options for the extraction and display of the thumbnail image.


## -enum-fields




### -field WTS_NONE

0x00000000. <b>Introduced in Windows 8</b>. None of the following options are set.


### -field WTS_EXTRACT

Default. 0x00000000. Extract the thumbnail if it is not cached.


### -field WTS_INCACHEONLY

0x00000001. Only return the thumbnail if it is cached.


### -field WTS_FASTEXTRACT

0x00000002. If not cached, only extract the thumbnail if it is embedded in EXIF format, typically 96x96.


### -field WTS_FORCEEXTRACTION

0x00000004. Ignore cache and extract thumbnail from source file.


### -field WTS_SLOWRECLAIM

0x00000008. The thumbnail has an extended lifetime. Use for volumes that might go offline, like non-fixed disks.


### -field WTS_EXTRACTDONOTCACHE

0x00000020. Extract but do not add the thumbnail to the cache.


### -field WTS_SCALETOREQUESTEDSIZE

0x00000040. <b>Introduced in Windows 7</b>. If the specific thumbnail size requested in the <i>cxyRequestedThumbSize</i> parameter is not available, resize the thumbnail to the requested size. If possible, a larger bitmap is reduced in scale, preserving its aspect ratio, to the width and height required. If the only available cached thumbnail is smaller than the requested size, then it is scaled up using the nearest-neighbor algorithm.


### -field WTS_SKIPFASTEXTRACT

0x00000080. <b>Introduced in Windows 7</b>. Do not extract a thumbnail embedded in the metadata of an EXIF image.


### -field WTS_EXTRACTINPROC

0x00000100. <b>Introduced in Windows 7</b>. Ensures that the thumbnail handler is loaded in the same process as the caller. When this flag is not specified, the handler is loaded into a surrogate process to protect the caller from unexpected crashes caused by the processing of the target file. Use this value when debugging thumbnail extractors.


### -field WTS_CROPTOSQUARE

0x00000200. <b>Introduced in Windows 8</b>. If necessary, crop the bitmap's dimensions so that is square. The length of the shortest side becomes the length of all sides.


### -field WTS_INSTANCESURROGATE

0x00000400. <b>Introduced in Windows 8</b>. Create a surrogate for this instance of the cache rather than using the shared DLLHost surrogate.


### -field WTS_REQUIRESURROGATE

0x00000800. <b>Introduced in Windows 8</b>. Require extractions to take place in the surrogate.


### -field WTS_APPSTYLE

0x00002000. <b>Windows 8 and later</b>. Pass the <a href="https://msdn.microsoft.com/062B148E-19FB-4bcd-82CE-669B2ACD0BF6">WTSCF_APPSTYLE</a> flag to <a href="https://msdn.microsoft.com/AD333075-3358-4fee-BDEE-087B7012C93E">IThumbnailSettings::SetContext</a>, if the provider supports it.  



### -field WTS_WIDETHUMBNAILS

0x00004000. <b>Windows 8 and later</b>. Stretch and crop the bitmap so that its height is 0.7 times its width.


### -field WTS_IDEALCACHESIZEONLY

0x00008000. <b>Windows 8 and later</b>. Return from the ideal cache snap size only. The returned image might be larger, but it will be pulled from the correct cache entry.  


### -field WTS_SCALEUP

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




<a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a>



<a href="https://msdn.microsoft.com/AD333075-3358-4fee-BDEE-087B7012C93E">IThumbnailSettings::SetContext</a>
 

 

