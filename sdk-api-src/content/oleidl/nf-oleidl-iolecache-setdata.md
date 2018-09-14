---
UID: NF:oleidl.IOleCache.SetData
title: IOleCache::SetData
author: windows-sdk-content
description: Initializes the cache with data in a specified format and on a specified medium.
old-location: com\iolecache_setdata.htm
tech.root: com
ms.assetid: b826411d-6e00-44ba-8603-85db40c4a55f
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IOleCache interface [COM],SetData method, IOleCache.SetData, IOleCache::SetData, SetData, SetData method [COM], SetData method [COM],IOleCache interface, _ole_iolecache_setdata, com.iolecache_setdata, oleidl/IOleCache::SetData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleCache.SetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleCache::SetData


## -description


Initializes the cache with data in a specified format and on a specified medium.


## -parameters




### -param pformatetc [in]

A pointer to a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that specifies the format of the presentation data being placed in the cache.


### -param pmedium [in]

A pointer to a <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> structure that specifies the storage medium that contains the presentation data.


### -param fRelease [in]

Indicates the ownership of the storage medium after completion of the method. If <i>fRelease</i> is <b>TRUE</b>, the cache takes ownership, freeing the medium when it is finished using it. When <i>fRelease</i> is <b>FALSE</b>, the caller retains ownership and is responsible for freeing the medium. The cache can only use the storage medium for the duration of the call.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>lindex</b>. Currently, only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_TYMED</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>tymed</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>dwAspect</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
There is an uninitialized object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_TARGETDEVICE</b></dt>
</dl>
</td>
<td width="60%">
The object is static and <i>pformatetc</i>-&gt;<b>ptd</b> is non-<b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The storage medium is full.

</td>
</tr>
</table>
 




## -remarks



<b>IOleCache::SetData</b> is usually called when an object is created from the clipboard or through a drag-and-drop operation, and Embed Source data is used to create the object.

<b>IOleCache::SetData</b> and <a href="https://msdn.microsoft.com/4b1f2fb6-636c-47dd-8f89-884f7b4f3977">IOleCache::InitCache</a> are very similar. There are two main differences. The first difference is that while <b>IOleCache::InitCache</b> initializes the cache with the presentation format provided by the data object, <b>IOleCache::SetData</b> initializes it with a single format. Second, the <b>IOleCache::SetData</b> method ignores the ADVF_NODATA flag while <b>IOleCache::InitCache</b> obeys this flag.

A container can use this method to maintain a single aspect of an object, such as the icon aspect of the object.




## -see-also




<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>



<a href="https://msdn.microsoft.com/b826411d-6e00-44ba-8603-85db40c4a55f">IOleCache::SetData</a>
 

 

