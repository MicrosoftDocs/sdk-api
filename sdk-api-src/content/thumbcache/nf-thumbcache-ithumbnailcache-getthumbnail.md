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

# IThumbnailCache::GetThumbnail


## -description


Gets a cached thumbnail for a given Shell item.


## -parameters




### -param pShellItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the Shell item for which to retrieve a thumbnail.


### -param cxyRequestedThumbSize [in]

Type: <b>UINT</b>

The requested thumbnail size in pixels. The maximum value is 1024.


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_FLAGS</a></b>

A combination of values from the <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_FLAGS</a> enumeration. See the Remarks section for rules and a list of possible combinations.


### -param ppvThumb [out, optional]

Type: <b><a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a>**</b>

The address of an <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> pointer that, when this method returns successfully, receives the object used to access the thumbnail. This parameter may be <b>NULL</b>.


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

Type: <b><a href="https://msdn.microsoft.com/3006d1a8-c9cf-4528-9aea-8ad5d97ddff0">WTS_THUMBNAILID</a>*</b>

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
 


<a href="https://msdn.microsoft.com/b31a5eb7-f12f-41e0-9047-450240371424">GetImage</a> also uses this cache and can provide an easier way to retrieve the thumbnail. However, <b>GetImage</b> is more general and will retrieve an icon as a fallback.




## -see-also




<a href="https://msdn.microsoft.com/b31a5eb7-f12f-41e0-9047-450240371424">IShellItemImageFactory::GetImage</a>



<a href="https://msdn.microsoft.com/b0ddfca0-49b8-4f53-8d22-9a561d09367a">IThumbnailCache</a>
 

 

