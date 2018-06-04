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

# IThumbnailCache::GetThumbnailByID


## -description


Gets a thumbnail from the thumbnail cache, given its ID.


## -parameters




### -param thumbnailID [in]

Type: <b><a href="https://msdn.microsoft.com/3006d1a8-c9cf-4528-9aea-8ad5d97ddff0">WTS_THUMBNAILID</a></b>

The ID of the thumbnail to retrieve. The ID is obtained by calling <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">GetThumbnail</a>.


### -param cxyRequestedThumbSize [in]

Type: <b>UINT</b>

The requested thumbnail size in pixels. This value cannot be larger than 1024.


### -param ppvThumb [out, optional]

Type: <b><a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a>**</b>

The address of a <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> interface pointer that, when this method returns successfully, receives the object for accessing the requested thumbnail. This parameter can be <b>NULL</b>.


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



This method is typically called after <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">GetThumbnail</a> has already been called to retrieve the thumbnail ID.



